# BOERDARIJA Product Improvement Roadmap

## Core direction

BOERDARIJA should evolve from a broad static Darija learning site into a **sleek, useful, scenario-driven Casablanca Darija product** that helps people:

- survive daily life in Casablanca
- understand how people actually speak
- learn slang and natural phrasing without sounding ridiculous
- build confidence through roleplay, audio, and short playful interactions

---

## Phase 1 — Quick wins (1-3 days)

### 1. Fix obvious structural bugs
- Add `js/navigation.js` to `index.html` so nav loads properly
- Fix or remove broken `resources.html` breadcrumb in `dictionary.html`
- Run a simple internal-link audit and fix dead links
- Verify home, courses, dictionary, vocabulary game, and lesson navigation all work cleanly

### 2. Clarify homepage positioning
Replace generic copy with sharper messaging around:
- Casablanca dialect focus
- practical real-life use
- slang / natural speech
- scenario learning

Suggested homepage positioning:
- **Learn Casablanca Darija the way people actually speak it.**
- Roleplays, slang, useful phrases, and real-life situations.

### 3. Clean repo basics
- Remove obvious junk / temp files from root (or move into `logs/` / `scripts/` / `docs/`)
- Move push scripts and maintenance scripts into dedicated folders
- Group audio logs/status files so the root is not chaotic
- Add a simple top-level repo map in README

### 4. Define product pillars in docs
Create one short vision doc that defines the four product pillars:
- survival phrases
- real Casablanca speech
- scenario roleplays
- micro-play / games

---

## Phase 2 — Product identity pass (3-7 days)

### 5. Redesign the homepage around use cases
Homepage should quickly route users into:
- **Start with useful situations**
- **Learn key phrases**
- **Browse slang**
- **Play a short game**
- **Search the dictionary**

### 6. Introduce a new "Scenarios" section
Create a dedicated scenarios hub with initial cards such as:
- Taxi
- Café
- Market / bargaining
- Greetings with family/friends
- Asking for directions
- Saying you don’t understand
- WhatsApp / texting style
- Rent / apartment / landlord basics

### 7. Add “natural vs textbook vs slang” framing
For selected phrases, show:
- safe/basic version
- natural Casablanca version
- slangy version
- warning note if something sounds too formal / weird / old-school

### 8. Improve visual polish
- Make the design feel more premium / sleek / urban
- Reduce “generic course site” energy
- Add stronger card layouts and cleaner call-to-actions
- Tighten typography hierarchy and spacing

---

## Phase 3 — Content architecture (1-2 weeks)

### 9. Build the first 20 scenario roleplays
Prioritize practical situations:
1. greeting casually
2. meeting someone new
3. café ordering
4. asking taxi price/destination
5. bargaining in a market
6. asking for directions
7. saying “I don’t understand” / “repeat slowly”
8. buying groceries
9. family visit basics
10. small talk with neighbors
11. arranging to meet by WhatsApp
12. apologizing / being polite
13. refusing politely
14. landlord / apartment basics
15. asking for help
16. delivery / phone call basics
17. joking / casual banter
18. health / pharmacy basics
19. beach / travel outing basics
20. social invitation and response

### 10. Create a slang layer
Add a structured system for slang labels such as:
- common
- casual
- playful
- rude-ish
- old-school
- textbook
- Casablanca-specific

### 11. Add mini-story content
Short stories can reinforce tone and context:
- market misunderstanding
- awkward taxi interaction
- family lunch scene
- WhatsApp voice note confusion
- first time bargaining badly

---

## Phase 4 — Audio strategy (1-2 weeks, careful use of credits)

### 12. Use ElevenLabs credits intentionally
Prioritize audio for:
- scenario dialogues
- highly useful phrases
- slang contrasts
- listening mini-tests
- short story scenes

Avoid spending credits on low-value one-off vocabulary unless strategically important.

### 13. Create consistent audio standards
Define:
- naming convention
- folder structure
- metadata / mapping rules
- voice/tone policy
- which content types deserve audio first

### 14. Add better audio UX
Eventually support:
- play buttons for key lines
- replay line-by-line in dialogues
- hover audio only where it really helps
- maybe “slow replay” for difficult lines later

---

## Phase 5 — Game and interaction upgrades (1-2 weeks)

### 15. Upgrade from vocab quiz to situation micro-games
Replace or complement vocab quiz with:
- pick the natural reply
- what would a real Casawi say?
- slang match game
- tone recognition
- reorder a short dialogue
- choose the least weird option

### 16. Add scenario branching
Very light branching roleplays:
- user picks a response
- gets tone/context feedback
- sees a more natural option

This would make BOERDARIJA feel much more alive than a normal course site.

---

## Phase 6 — Technical cleanup (parallel or later)

### 17. Reduce lesson duplication
- Move repeated styles into shared CSS
- Move repeated nav/footer/breadcrumb logic into reusable includes or patterns
- Reduce inline styles where practical

### 18. Organize repo structure
Recommended structure:
- `docs/`
- `scripts/`
- `logs/`
- `audio/`
- `data/`
- `css/`
- `js/`
- root only for actual site pages if staying static

### 19. Improve documentation
- update README
- add product vision doc
- add content roadmap doc
- add audio workflow doc
- add lightweight contributor notes for future-you

### 20. Add license
Even a simple license is better than ambiguity.

---

## Priority order if you want fastest real progress

### Top 5 in order
1. Fix broken structural/navigation issues
2. Rewrite homepage positioning around Casablanca + real-life use
3. Create a Scenarios hub
4. Define the first 20 roleplays
5. Add natural vs textbook vs slang presentation

---

## Best immediate next tasks

If working right now, the best first sprint is:

### Sprint A
- fix homepage nav
- fix broken dictionary breadcrumb
- tighten homepage copy
- create a `SCENARIOS.md` planning doc with the first 20 scenario ideas

### Sprint B
- build the first actual Scenarios page
- add 3 pilot scenarios
- test tone/style before expanding

---

## Success test

BOERDARIJA is getting more compelling if a new visitor quickly thinks:

> “Oh, this is not generic Arabic learning. This is specifically for helping me function and sound human in Casablanca.”

That should be the bar.
