# Sticker posters

Getting-to-know-each-other posters, based on Christian's hand-drawn sketch of 18 November 2026. Printable versions are in `posters.html`.

## Sticker rules

- **One sticker colour per institution:** TU/e, CWI, VU, UvA, RU, plus a sixth colour for other / guests. Each poster has an empty legend in its header: before hanging, put one sticker of each colour next to the institution's name.
- **One sticker per person per poster**, except:
  - Poster 1 (core challenges): **two** stickers per person.
  - Posters 5 and 7 (verification tools, AI models): **as many as apply**.
- Stickers aren't anonymous by name, but they are by colour. Speak to someone with a sticker near yours.

## The posters

| # | Question | Layout |
|---|---|---|
| 1 | Which core challenges are closest to your work? | 3×3 grid: columns Crypto / HW / SW, holding the nine CiCS core challenges |
| 2 | Where did you go to primary school? | World map, enlarged Europe, and a wide enlarged map of the Netherlands and surroundings (Belgium, western Germany) with university cities |
| 3 | Where did you get – or are you doing – your PhD? | Same maps as poster 2; current PhD students place their sticker at their current university |
| 4 | Where do you feel most at home? | Thematic map of publication venues: 4 columns (theory, cryptography, security & privacy, AI/data/systems) × 3 rows (foundations → applied → engineering/journals), 12 named topic areas. CiCS venues are bold with their paper count; well-known venues without CiCS papers yet (CRYPTO, STOC, FOCS, …) are included too. Empty boxes for anything else |
| 5 | Formal verification: which tools have you ever used? | Grouped: proof assistants (Lean, Rocq, Isabelle, Agda, HOL4/CakeML); cryptographic proofs & code (EasyCrypt, Jasmin, CryptoVerif, SSProve, F*/HACL*, Cryptol/SAW, hax); protocols (ProVerif, Tamarin, Squirrel); programs & systems (Dafny, Why3, Verus/Kani, TLA+, SMT solvers); plus other and unfamiliar |
| 6 | AI: how often do you use AI for research? | never → sometimes → always, one row per career stage (PhD student, postdoc, faculty, other) |
| 7 | AI: which models do you use? | Claude, ChatGPT, Gemini, Mistral, open-weight, self-trained, other |
| 8 | AI tools and agents: how much do you let them do? | 2-D, axes crossing in the middle: how often you use AI tools in general (never → always) against how you run agents (no agents → manual approval → auto mode → sandboxed, unattended → YOLO) |
| 9 | Are you worried about AI developments? | 2-D, axes crossing in the middle: worry about job security (x) against worry about existential risk (y) |

## Notes

- The placement of the nine challenges in the Crypto / HW / SW columns follows the TU/e kick-off article as read in CiCS-output (`project/overview.md`). There, the third pillar is called "physical security" and the order is Crypto / SW / physical. Check with Tanja that the placement is right.
- The CiCS paper counts on poster 4 come from `publications/publications.json` in CiCS-output (79 papers, as of 18 November 2026). Preprint servers, datasets and reports are left out. The placement of venues in topic areas is a judgement call (e.g. SPACE and DATE under crypto engineering & hardware, IWSPA under data & analytics, CSF under formal methods) and easy to change in `VENUE_MAP`.
- Poster 5: Formosa from the sketch is left out, because it is a project (around EasyCrypt and Jasmin) rather than a tool. Additions beyond the sketch: Agda, HOL4/CakeML, CryptoVerif, SSProve, F*/HACL*, Cryptol/SAW, hax, ProVerif, Tamarin, Squirrel, Dafny, Why3, Verus/Kani, TLA+, SMT solvers. Trim to taste in `FV`.
- The maps need internet access when printing: wait until they appear before printing. They use public-domain Natural Earth outlines, loaded from jsdelivr with integrity hashes. If loading fails, a red note appears at the top of the page.
