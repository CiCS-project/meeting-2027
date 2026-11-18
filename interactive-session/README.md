# Interactive session: sticker posters and CiCS priorities

Material for the CiCS meeting of 27 January 2027. Nine posters invite everyone to place stickers in their institution's colour: research challenges, where people come from, favourite venues, formal-verification tools, and AI use and worries. The patterns help people find each other and seed the discussion on CiCS priorities.

This folder is excluded from the website build (see `exclude` in `_config.yml`). The repository itself is public, so don't put anything confidential here.

| File | What |
|---|---|
| `README.md` | This facilitation guide: timeline, roles, materials checklist |
| `posters.md` | **What each poster asks**, sticker rules, open points |
| `posters.pdf` | **Ready-to-print PDF** of all 9 posters (A3 landscape; scale up to A2/A1 at a print shop). Regenerate after editing `posters.html` (see below) |
| `posters.html` | Printable posters, one per page (open in a browser, wait for the maps, then Print → A3 landscape, margins none; a print shop can scale them up to A2/A1) |
| `group-sheet.md` | One-page worksheet per small group |
| `results.md` | Template for recording the outcome after the meeting |

## Timeline

| Time | What | Who |
|---|---|---|
| Before 12:30 | Hang the 9 posters along one wall. Fill in each colour legend with one sticker per colour. Put sticker sheets at the registration desk. | Organisers |
| 12:30 | Everyone gets a strip of stickers in their institution's colour at registration. Mention the posters briefly in the welcome. | Organisers, Tanja |
| 13:15 – 13:30 | **Sticker round.** Everyone places their stickers on the 9 posters (instructions below). | Everyone |
| 13:30 – 14:30 | **Speed meeting.** The posters serve as prompts: "Find someone whose sticker is near yours on poster X", or "… from another institution on the same challenge". | Everyone |
| 14:30 – 14:50 | **Coffee break.** Last chance to place stickers. | Everyone |
| 14:50 – 15:20 | **Walk past the posters together**, about 3 minutes per poster. A facilitator describes the colour patterns: where institutions cluster, where they overlap, and any surprises. One or two people briefly explain an outlier. | Facilitators |
| 15:20 – 16:00 | **Small groups around shared challenges.** On poster 1, pick the 4–6 challenge cells with stickers from at least 3 institutions. One group per cell (5–8 people, mixed) asks: *what could we do together on this?* Each group fills in `group-sheet.md`. | Groups, each with a note-taker |
| 16:00 – 16:20 | Coffee break and networking | |
| 16:20 – 16:50 | **Report back:** 3–4 minutes per group (conclusion, one concrete next step, who drives it), then a plenary discussion of which next steps CiCS adopts. | Groups; chair: a PI |

## Roles

- **Chair** (a PI): keeps time, runs the report-back and closes with the list of next steps.
- **Facilitators** (2–3 people): describe the posters during the walk-along.
- **Note-takers**: one per group.
- **Photographer**: photographs each poster at 14:50, before the discussion starts.

## Materials checklist

- [ ] 9 posters printed (A2 or A1, or A3 for small groups); print the map posters while online
- [ ] Round dot stickers (about 12–15 mm) in **6 colours**, about 20 per person (about 700 in total for 35 people). Pre-cut strips of about 20 per person, one colour per institution.
- [ ] Thin markers for writing on the "other: …" fields
- [ ] Masking tape or poster putty; check with the VU room whether walls or boards may be used
- [ ] Printed group sheets (6 plus spares)
- [ ] Timer and bell

## Instructions to read out in the welcome

1. Your stickers have your institution's colour. Place one per poster (two on the challenges poster; as many as apply on the verification-tools and AI-models posters).
2. Place them during the sticker round at 13:15, or later in the coffee break, but before 14:50.
3. Use the posters to find people. If your sticker is next to someone else's, go and talk to them.

## Regenerating `posters.pdf`

After editing `posters.html`, run this from the repository root (it needs internet access for the maps):

```sh
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --disable-gpu --no-pdf-header-footer \
  --virtual-time-budget=20000 --print-to-pdf=interactive-session/posters.pdf \
  "file://$PWD/interactive-session/posters.html"
```

Check that the maps on posters 2 and 3 are visible before committing.
