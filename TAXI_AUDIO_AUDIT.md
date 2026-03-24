# Taxi Basics Audio Audit

This is the first-pass audit for a future **Taxi Basics** scenario page.

Goal:
- identify which high-value taxi phrases already have audio coverage
- identify which phrases are partially covered / adaptable from existing content
- identify what is genuinely worth generating with ElevenLabs

---

## Summary

**Good news:** the repo already contains enough relevant audio to build a meaningful first Taxi Basics scenario without generating everything from scratch.

There is already coverage for:
- greetings
- please / thank you / excuse me
- near / far
- taxi vocabulary
- some direction/location phrases
- some “where is...?” patterns
- some waiting / negotiation language
- some future/going movement language (`ghadi`, `ghadi nmshi`)

That means we should **reuse first, generate second**.

---

## 1. Already covered cleanly

These appear to have clear existing audio coverage in either `audio/` or `audio/lessons/`.

### Core politeness / taxi setup
- `Salam` → `audio/salam.mp3`
- `Afak` → `audio/afak.mp3`
- `3afak` → `audio/3afak.mp3`
- `Shukran` → `audio/shukran.mp3`
- `Smehli` → `audio/smehli.mp3`
- `Taxi` → `audio/taxi.mp3`

### Direction / distance basics
- `Qrib` → `audio/qrib.mp3`
- `B3id` → `audio/b3id.mp3`
- `Qddam` → `audio/lessons/qddam.mp3`
- `Shwiya` → `audio/lessons/shwiya.mp3`

### Useful support phrases already present in lesson audio
- `ghadi_nmshi` → `audio/lessons/ghadi_nmshi.mp3`
- `wash_qrib` → `audio/lessons/wash_qrib.mp3`
- `wash_b3id` → `audio/lessons/wash_b3id.mp3`
- `qrib_mn_hna` → `audio/lessons/qrib_mn_hna.mp3`
- `b3id_mn_hna` → `audio/lessons/b3id_mn_hna.mp3`
- `belati_tsenna_shwiya` → `audio/lessons/belati_tsenna_shwiya.mp3`
- `neqqs_shwiya_3afak` → `audio/lessons/neqqs_shwiya_3afak.mp3`
- `shukran_bzzaf` → `audio/lessons/shukran_bzzaf.mp3`
- `la_shukran_khllih` → `audio/lessons/la_shukran_khllih.mp3`

### Location-question patterns already present
- `fin_l_m7atta` → `audio/lessons/fin_l_m7atta.mp3`
- `fin_l_farmasiyan` → `audio/lessons/fin_l_farmasiyan.mp3`
- `fin_s_souq` → `audio/lessons/fin_s_souq.mp3`

These are useful because they prove the product already has viable “where is / where to” patterns.

---

## 2. Partially covered / reusable with slight adaptation

These do not appear as exact perfect taxi lines, but there is enough nearby coverage to make them easy to build around.

### “I want to go to X”
Target line:
- `Bghit nmshi l-...`

Current state:
- `ghadi_nmshi.mp3` exists
- `bgheet.mp3` exists in root audio as a close useful piece

Meaning:
- we can likely build this with partial reuse in content terms
- but for polished scenario audio, a direct full-line recording would be better

### “Where to?” / “Where are you going?”
Target lines:
- `L-fin?`
- `Fin ghadi?`

Current state:
- multiple `fin_...` patterns exist
- many `ghadi...` patterns exist

Meaning:
- conceptually covered
- exact taxi-native line probably still worth recording later

### “Wait a bit”
Target line:
- `Tsenna shwiya`

Current state:
- `belati_tsenna_shwiya.mp3` exists

Meaning:
- probably already good enough for an early scenario
- exact shorter line could be generated later if we want cleaner minimal phrasing

### “Stop here” / “I get off here”
Target lines:
- `Wqef hna`
- `Nzel hna`

Current state:
- `waqef_waqfa.mp3` exists but is not the same thing

Meaning:
- this is **not really covered properly**
- should likely be generated

---

## 3. Best candidate phrases for first Taxi Basics page

Here is the first sensible phrase set.

### Tier A — use existing audio immediately
These are good enough to start with right now:
- Salam
- Afak / 3afak
- Shukran
- Smehli
- Taxi
- Qrib
- B3id
- Qddam
- Shwiya
- Wash qrib?
- Wash b3id?
- Qrib mn hna
- B3id mn hna
- Belati, tsenna shwiya
- Neqqs shwiya, 3afak

### Tier B — useful but should ideally get full-line scenario audio
- Bghit nmshi l-...
- Fin ghadi?
- L-fin?
- Bshal?
- Wqef hna
- Nzel hna
- 3la l-ymin
- 3la l-ysar
- Ma fhemtsh
- 3awed, 3afak

---

## 4. What is worth generating with ElevenLabs first

If we are spending credits carefully, these are the **high-value missing lines** I would generate first for a Taxi Basics scenario:

### Priority 1 — must-have scenario lines
1. `Bghit nmshi l-...` — I want to go to ...
2. `L-fin?` — To where?
3. `Fin ghadi?` — Where are you going?
4. `Bshal?` — How much?
5. `Wqef hna, 3afak.` — Stop here, please.
6. `Nzel hna.` — I’m getting off here.
7. `3la l-ymin.` — To the right.
8. `3la l-ysar.` — To the left.
9. `Ma fhemtsh.` — I didn’t understand.
10. `3awed, 3afak.` — Repeat, please.

### Priority 2 — nice-to-have roleplay lines
11. `Sir qddam.` — Go straight.
12. `Belati hna shwiya.` — Wait here a bit.
13. `Wash qrib wlla b3id?` — Is it near or far?
14. `Hna mzyan, shukran.` — Here is fine, thanks.
15. `Ma 3ndich srraf.` — I don’t have change.

---

## 5. What not to generate yet

Avoid generating these immediately if credits matter:
- single words already covered (`Salam`, `Shukran`, `Afak`, `Qrib`, `B3id`)
- generic words that already exist in dictionary audio
- phrases we may later rewrite after scenario design settles

The goal is not “more audio.”
The goal is **better scenario usefulness per credit**.

---

## 6. Recommendation

For the first Taxi Basics scenario page:

### Use existing audio now for:
- politeness
- distance
- general movement support lines

### Generate new audio only for:
- destination request
- cost question
- stop/get off lines
- left/right
- understanding repair lines

That gives us a page that already feels alive without wasting credits on obvious duplicates.

---

## 7. Best next step

Next practical move:
- draft the Taxi Basics scenario page content
- plug in the already-covered audio lines
- mark the 10 missing high-value lines for ElevenLabs generation

That will give BOERDARIJA its first truly scenario-native audio page.
