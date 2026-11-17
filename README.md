# CiCS Meeting – 27 January 2027

Website for the meeting of **Challenges in Cyber Security (CiCS)**, an NWO Gravitation project.

- **Date:** Wednesday, 27 January 2027, 12:30 – 17:30, followed by drinks
- **Location:** Vrije Universiteit Amsterdam (room to be announced)
- **Registration:** <https://hyperelliptic.org/tanja/c896aa4b90aee4a9a69d5b059a0570451b53a4c9-reg.html>
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
