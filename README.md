# CiCS Meeting – 27 January 2027

Website for the meeting of **Challenges in Cyber Security (CiCS)**, an NWO Gravitation project.

- **Date:** Wednesday, 27 January 2027, 12:30 – 17:30, followed by drinks
- **Location:** Vrije Universiteit Amsterdam (room to be announced)
- **Registration:** <https://cryptpad.fr/form/#/2/form/view/d-FrQ-Tqb-tQkW5K+PJRydmjYejnx3B9NAYOYdB1E+o/>
- **Registration responses:** CryptPad form owned by the organisers' CryptPad account (cryptpad.fr, end-to-end encrypted). Export via the form's *Responses* view → export as CSV; delete the form after the meeting.
- **Live page:** <https://cics-project.github.io/meeting-2027/>

## Editing

The page is built by GitHub Pages with Jekyll on every push to `main` (no local build needed; it is live within a minute or two).

| What to change | File |
|---|---|
| Program: sessions, times, titles, speakers, breaks | `_data/program.yml` |
| Date, time, location, registration link, project name | `_config.yml` |
| Page structure (HTML) | `index.html`, `_layouts/default.html` |
| Styling | `assets/style.css` |

In `_data/program.yml`, each item has a `time`, a `title`, an optional `detail` (e.g. speaker), and `break: true` for coffee/drinks rows.

To preview locally (optional): `gem install jekyll && jekyll serve`, then open <http://localhost:4000/meeting-2027/>.
