# BOERDARIJA Scenario Audio Pattern

This document defines the reusable audio/content block for future scenario pages.

The goal is to make scenario pages:
- easy to read
- easy to hear
- easy to expand
- easy to wire to audio
- much less manually repetitive than the current lesson pages

---

## Core idea

Each scenario page should be built from **compact conversation blocks** rather than giant custom tables.

Each block should support:
- Darija line
- transliteration
- English meaning
- optional usage note
- audio play button
- optional tags like `natural`, `slang`, `safe`, `formal`

This gives us one clean pattern for:
- phrase cards
- mini dialogues
- roleplays
- listening practice
- natural vs textbook comparisons

---

## Recommended UI block types

### 1. Phrase card
Best for:
- key survival phrases
- quick phrase packs
- high-frequency expressions

### 2. Dialogue turn
Best for:
- roleplays
- taxi/café/market exchanges
- short stories

### 3. Contrast card
Best for:
- natural vs textbook vs slang
- safe vs risky phrasing
- polite vs casual

---

# 1. Phrase card pattern

## Visual structure
- Darija line (most prominent)
- transliteration beneath
- English meaning beneath that
- tag row
- play button
- optional note

## Suggested HTML pattern

```html
<div class="phrase-card" data-audio="audio/scenarios/taxi/fin_ghadi_lmaarif.mp3">
  <div class="phrase-main">
    <div class="phrase-arabic" lang="ar" dir="rtl">فين غادي للمعاريف؟</div>
    <div class="phrase-translit">fin ghadi l-Maarif?</div>
    <div class="phrase-meaning">Are you going to Maarif?</div>
  </div>

  <div class="phrase-meta">
    <span class="tag safe">safe</span>
    <span class="tag natural">natural</span>
    <span class="tag casablanca">casablanca</span>
  </div>

  <div class="phrase-actions">
    <button class="audio-btn" type="button" aria-label="Play audio">▶ Play</button>
  </div>

  <div class="phrase-note">
    Useful for checking direction or confirming destination with a taxi driver.
  </div>
</div>
```

## Why this is good
- compact
- reusable
- not table-heavy
- easy to style nicely
- audio can be wired by `data-audio`

---

# 2. Dialogue turn pattern

Best for conversations.

## Suggested HTML pattern

```html
<div class="dialogue-turn speaker-local" data-audio="audio/scenarios/taxi/salam_lfin_bghiti.mp3">
  <div class="speaker-label">Driver</div>
  <div class="dialogue-arabic" lang="ar" dir="rtl">سلام، لفين بغيتي؟</div>
  <div class="dialogue-translit">salam, l-fin bghiti?</div>
  <div class="dialogue-meaning">Hi, where do you want to go?</div>
  <button class="audio-btn" type="button">▶</button>
</div>

<div class="dialogue-turn speaker-learner" data-audio="audio/scenarios/taxi/bghit_nmshi_lmaarif.mp3">
  <div class="speaker-label">You</div>
  <div class="dialogue-arabic" lang="ar" dir="rtl">بغيت نمشي للمعاريف</div>
  <div class="dialogue-translit">bghit nmshi l-Maarif</div>
  <div class="dialogue-meaning">I want to go to Maarif.</div>
  <button class="audio-btn" type="button">▶</button>
</div>
```

## Why this is good
- feels like a real scene
- audio per line is natural
- easy to make roleplay pages feel alive
- works beautifully for story/scenario content

---

# 3. Contrast card pattern

This is one of BOERDARIJA’s future signature features.

Use it for:
- textbook vs natural
- safe vs slang
- formal vs real-life casual

## Suggested HTML pattern

```html
<div class="contrast-card">
  <h3>How a real person would say it</h3>

  <div class="contrast-option">
    <span class="tag textbook">textbook</span>
    <div class="contrast-line">أريد الذهاب إلى المعاريف</div>
    <div class="contrast-translit">urid adhhab ila l-Maarif</div>
    <div class="contrast-note">Technically understandable, but not how most people would say it in daily Casablanca speech.</div>
  </div>

  <div class="contrast-option">
    <span class="tag natural">natural</span>
    <div class="contrast-line">بغيت نمشي للمعاريف</div>
    <div class="contrast-translit">bghit nmshi l-Maarif</div>
    <div class="contrast-note">Safer and much more natural in real life.</div>
  </div>

  <div class="contrast-option">
    <span class="tag slang">slang</span>
    <div class="contrast-line">غادي للمعاريف؟</div>
    <div class="contrast-translit">ghadi l-Maarif?</div>
    <div class="contrast-note">More clipped and contextual — useful once the basics feel easy.</div>
  </div>
</div>
```

---

# Audio wiring pattern

## Recommended rule
Do **not** hardcode lots of `<audio id="..."></audio>` elements all over the page.

Instead:
- store the path in `data-audio`
- use one reusable JS handler
- play audio from the clicked card/button

## Suggested JS pattern

```js
document.addEventListener('click', (e) => {
  const button = e.target.closest('.audio-btn');
  if (!button) return;

  const block = button.closest('[data-audio]');
  if (!block) return;

  const src = block.dataset.audio;
  if (!src) return;

  const player = new Audio(src);
  player.play().catch(err => console.error('Audio play failed', err));
});
```

## Better version later
Eventually use a single shared audio player so sounds don’t overlap.

---

# File path convention for scenario audio

## Recommended folder structure

```text
audio/
  scenarios/
    taxi/
    cafe/
    market/
    directions/
    whatsapp/
```

Examples:
- `audio/scenarios/taxi/bghit_nmshi_lmaarif.mp3`
- `audio/scenarios/cafe/bghit_atay_bla_skar.mp3`
- `audio/scenarios/market/bshal_hadi.mp3`

## Why this matters
- easier to manage than dumping everything into root audio
- scenario content stays grouped
- easier to reuse later
- easier to regenerate selectively

---

# Tag system

Use lightweight tags to help learners understand tone.

## Suggested tags
- `safe`
- `natural`
- `slang`
- `textbook`
- `formal`
- `playful`
- `rude-ish`
- `casablanca`
- `high-frequency`

## Why tags matter
They make the project feel more human and practical.
Not just “what does this mean?” but:
- can I say this?
- when?
- to whom?
- how normal does it sound?

---

# Best pattern for first scenario pages

For early pages, use this layout:

## Scenario page structure
1. short intro
2. key phrases (phrase cards)
3. mini dialogue (dialogue turns)
4. natural vs textbook vs slang block
5. quick practice / mini challenge
6. cultural note / warning

This gives BOERDARIJA a clear product feel very quickly.

---

# Recommendation for the first implementation

For the first real scenario page (Taxi Basics):
- 8–12 phrase cards
- 1 short dialogue (4–6 turns)
- 1 contrast section
- audio only for high-value lines

That is enough to feel real without overbuilding.

---

# Summary

Use:
- **phrase cards** for survival language
- **dialogue turns** for roleplay
- **contrast cards** for natural vs textbook vs slang

And wire all audio through:
- `data-audio`
- shared `audio-btn`
- reusable JS

That will be much cleaner than the current lesson-by-lesson manual audio pattern.
