# BoerDarija Lab

An experimental **scenario-first Casablanca Darija** project.

This repo is the **lab / sandbox version** of BoerDarija. It is intentionally separate from the main project and is being used to explore a sharper product direction:

- more **Casablanca-specific**
- more **real-life situations**
- more **natural speech and slang**
- more **audio-driven roleplay**
- less generic course-site energy

## What this repo is
This repo is for experimenting with a version of BoerDarija that feels more like:

> a sleek, practical Casablanca Darija survival + social fluency tool

That means exploring things like:
- taxi / café / market / WhatsApp scenarios
- natural vs textbook vs slang phrasing
- scenario-native audio
- short roleplays, mini-stories, and small interaction loops
- more product-like UX ideas

## What this repo is **not**
This is **not** the canonical main BoerDarija repository.

The original/main project remains separate and may continue to evolve in a broader, more course-driven direction.

This lab exists so the two directions do not get mixed too early.

## Current focus
Right now this lab includes:
- improved homepage positioning toward real-life Casablanca use
- a new **Scenarios** layer
- a first real scenario page: **Taxi Basics**
- scenario audio experiments
- planning docs for roleplays, audio structure, and product direction

## Key files
- `index.html` — homepage / landing page
- `scenarios.html` — scenarios hub
- `scenario-taxi-basics.html` — first scenario prototype
- `SCENARIOS.md` — scenario roadmap
- `SCENARIO_AUDIO_PATTERN.md` — reusable scenario audio structure
- `TAXI_AUDIO_AUDIT.md` — first audio coverage audit
- `PRODUCT_ROADMAP.md` — staged improvement roadmap

## Repo hygiene / security
This repo now includes:
- `.gitignore` tuned for secret safety and local clutter
- `scripts/scan-secrets.sh` for lightweight secret scanning
- `scripts/install-git-hooks.sh` to install local pre-commit / pre-push checks
- `SECURITY.md` with the practical rules

To install the local hooks after cloning:

```bash
./scripts/install-git-hooks.sh
```

## Running locally
This is still a static-site style project.

To explore it:
1. clone the repo
2. open `index.html` in a browser
3. navigate into `scenarios.html` or the other pages

## Why keep this separate?
Because this version may eventually become a **different product** from the main BoerDarija project.

That is a feature, not a problem.
