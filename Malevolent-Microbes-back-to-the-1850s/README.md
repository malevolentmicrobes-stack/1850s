# Back to the 1850s?

Interactive teaching atlas for isolation precautions (Part 3): how long each pathogen lasts on surfaces, how hard it is to kill, how far it travels, and where routine practice misses it.

**Live site:** `https://malevolentmicrobes-stack.github.io/back-to-the-1850s/` (after GitHub Pages is turned on; see `docs/HANDOFF.md`)
**From:** [Malevolent Microbes](https://malevolentmicrobes-stack.github.io/cozy-arcade-app/)

## What's inside

A single self-contained page (`index.html`): no build step, no dependencies, works offline. Fonts load from Google Fonts when online and fall back to system sans-serif offline. Opens in dark mode; the toggle in the top bar switches to light.

| Tab | What it shows | Status |
|---|---|---|
| Home | Quantum orbital map: shells = disinfectant tier, sectors = route, cloud = persistence, beams = failed barriers | Final |
| Orbit | Routine tools as hubs; lines to the pathogens each one misses | Final |
| PPE | Gloves/gown, surgical mask, N95/AIIR, standard precautions vs. pathogens | Final |
| Agents | Alcohol, quats, bleach, H2O2 vs. the resistance ladder | Final |
| Three views | Orthographic drawing: time × space, time × disinfectant, space × disinfectant; color = fear | Final |
| Precaution game | 10 patients, choose room/surface/hands/mask; score, streak, lives, best score | Interactive |
| Barrier sim | Swiss-cheese lane with kit and skipped-step toggles | Interactive |
| Shield | Radial barrier rings; sectors sized by persistence | Interactive |
| Human factor | Hand-hygiene compliance slider (set to your unit's audit rate) | Interactive |
| Precaution rings, Route × time, Lasting vs tough, Failure map, Rose | Earlier drafts kept for comparison | Explored |

Tabs are hash-routed, so `index.html#game` or `#orbit` opens a tab directly.

## Repository layout

```
index.html              the app (everything inline)
assets/figures/         slide-ready PNGs of the static models (2720–3200 px)
docs/HANDOFF.md         terminal steps: git, GitHub, Pages, updating
docs/DATA.md            master data table, scoring rules, verification queue
```

## Evidence and limits

- Persistence values are laboratory ranges with high inocula (Kramer 2006 and others). They are not transmission or infection risk.
- "Fear" is a derived rule (what alcohol rub, routine wipe, or surgical mask misses), not a measured value.
- The game and models are teaching tools, not infection-control protocols. Follow institutional policy.
- Open verification items are listed in `docs/DATA.md`.

Key sources: CDC Guideline for Disinfection and Sterilization (2008), Fig. 1; CDC Isolation Precautions, Appendix A; EPA Lists G, K, P; Kramer 2006; Welsh 2017; Meister 2023; Mendis 2015; Lo 2026; Kociolek 2023; Lionakis 2024; Hall 2011; Mitchell 2015; Huang 2006.
