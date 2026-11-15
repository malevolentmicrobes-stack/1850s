# Data dictionary and master table

## Variables

| Variable | Meaning | Values | Source |
|---|---|---|---|
| tier (disinfectant) | CDC resistance hierarchy | 1 enveloped virus · 2 vegetative bacteria · 3 fungi · 4 non-enveloped virus · 5 mycobacteria · 6 spores | CDC 2008 Fig. 1 |
| space (route) | How far it travels | contact · droplet · airborne · water system | CDC Appendix A |
| persistence | Lab persistence on dry surfaces | range, single value, lower bound, or room-air time | Kramer 2006 and others |
| barrier states | Does a barrier stop it? | B blocks · L leaks / product-dependent · F fails · NA not the route · U unknown | per row |
| fear (derived) | What routine practice misses | red if a routine barrier fails on its route; amber if one leaks; otherwise "works if the step is done" | rule |

## Master table

Status: **V** verified against source · **U** from lecture source document, not independently checked · **X** check before use.

| Organism | Tier | Route | Persistence | Hand rub | Routine wipe | Surgical mask | N95/AIIR | Water program | Fear | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| C. difficile | 6 | contact | 5 mo (single value) | F | F* | NA | NA | NA | red | V |
| M. tuberculosis | 5 | airborne | not a fomite route | NA | NA | F | B | NA | red | route X |
| Adenovirus | 4 | droplet + contact | 7 d–3 mo | U | L* | B | B | NA | amber | persistence V; barriers X |
| Hepatitis A | 4 | contact (enteric) | 2 h–60 d | U | L* | NA | NA | NA | amber | persistence V |
| Norovirus | 4 | contact (enteric) | 8 h–7 d | L | L* | NA | NA | NA | amber | V |
| C. auris | 3 | contact | ≥14 d on plastic | B | F* | NA | NA | NA | red | V |
| MRSA | 2 | contact | 7 d–7 mo | B | B | NA | NA | NA | works | V |
| VRE | 2 | contact | 5 d–4 mo | B | B | NA | NA | NA | works | V |
| Acinetobacter | 2 | contact | 3 d–5 mo | B | B | NA | NA | NA | works | V |
| Pseudomonas | 2 | contact + drains | 6 h–16 mo | B | B | NA | NA | L | works | V |
| Klebsiella / CPE | 2 | contact + drains | 2 h to >30 mo | B | B | NA | NA | L | works | V |
| Legionella | 2 | water system | ≥208 d (lab freshwater) | NA | NA | NA | NA | B (room cleaning F) | red | Mendis U; Bartley V |
| Mpox | 1 | contact | ≤11 d (22 °C), ≤30 d (4 °C) | B | L* | X | X | NA | amber | persistence V; PPE X |
| Hepatitis B | 1 | blood/contact | >1 wk | B (U) | B | NA | NA | NA | works | persistence V |
| Influenza | 1 | droplet | 1–2 d | B | B | B | B | NA | works | persistence V |
| Measles | 1 | airborne | ~2 h in room air | B (U) | B | F | B | NA | red | Lo 2026 |

\* Product-dependent: the right EPA label claim (List G, K, P) or a sporicide turns it to B.

## Game scoring (Precaution game tab)

- Stopped: +100, plus 20 × current streak
- Leaked: +40, streak resets
- Spread: 0, lose one of 3 lives
- Overkill: −15 for an unneeded AIIR or N95, −10 for an unneeded water program
- Busy shift: 30% chance a performed hand or surface step is skipped; points ×1.5
- All routes a pathogen uses must be covered (parallel, not series)
- C. difficile is scored for an outbreak / hyperendemic setting (soap and water preferred; Kociolek 2023)

## Verification queue

1. CDC Appendix A entries for TB, measles, adenovirus, MDROs, mpox.
2. C. auris precaution category (CDC C. auris guidance).
3. Hand-rub efficacy against HAV and adenovirus (currently U).
4. Mpox PPE (N95) per current CDC guidance.
5. Legionella ~30% healthcare-associated case fatality (Barrier sim, Shield).
6. Lecture-document claims not re-checked: alcohol on adenovirus (5 min), 70% ethanol vs HAV, quats vs adenovirus.
7. Measles R0 12–18 and ~90% attack rate; norovirus 18–1,000 particles: trace to primary papers.

## References with links

- CDC. Guideline for Disinfection and Sterilization in Healthcare Facilities, 2008. https://www.cdc.gov/infection-control/hcp/disinfection-and-sterilization/resistance.html
- CDC. Isolation Precautions, Appendix A. https://www.cdc.gov/infection-control/hcp/isolation-precautions/appendix-a-type-duration.html
- US EPA. Antimicrobial products registered for claims against common pathogens. https://www.epa.gov/pesticide-registration/selected-epa-registered-disinfectants
- Kramer A, Schwebke I, Kampf G. BMC Infect Dis. 2006;6:130. https://doi.org/10.1186/1471-2334-6-130
- Kramer A, et al. Clin Microbiol Rev. 2024;37(4):e00186-23. https://doi.org/10.1128/cmr.00186-23
- McDonnell G, Russell AD. Clin Microbiol Rev. 1999;12(1):147-79. https://doi.org/10.1128/CMR.12.1.147
- Welsh RM, et al. J Clin Microbiol. 2017;55(10):2996-3005. https://doi.org/10.1128/JCM.00921-17
- Lionakis MS, Chowdhary A. N Engl J Med. 2024;391:1924-35. https://doi.org/10.1056/NEJMra2402635
- Meister TL, et al. J Infect Dis. 2023;228(9):1227-30. https://doi.org/10.1093/infdis/jiad127
- Lo NC. Measles. Ann Intern Med. 2026. https://doi.org/10.7326/ANNALS-26-03912
- Mitchell BG, et al. J Hosp Infect. 2015;91(3):211-7. https://doi.org/10.1016/j.jhin.2015.08.005
- Huang SS, Datta R, Platt R. Arch Intern Med. 2006;166:1945-51. https://doi.org/10.1001/archinte.166.18.1945
- Kociolek LK, et al. Infect Control Hosp Epidemiol. 2023;44:527-49. https://doi.org/10.1017/ice.2023.18
- Hall AJ, et al. MMWR Recomm Rep. 2011;60(RR-3). https://www.cdc.gov/mmwr/preview/mmwrhtml/rr6003a1.htm
- Mendis N, et al. PLoS One. 2015. https://doi.org/10.1371/journal.pone.0139277 (U)
- Bartley PB, et al. Clin Infect Dis. 2016;62(3):273-9. https://doi.org/10.1093/cid/civ870
- Hayward C, et al. Front Microbiol. 2025;16:1575789. https://doi.org/10.3389/fmicb.2025.1575789
- León-Sampedro R, et al. Nat Microbiol. 2021;6:606-16. https://doi.org/10.1038/s41564-021-00879-y
