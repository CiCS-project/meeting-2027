# CiCS Meeting – 27 January 2027

Website for the meeting of **Challenges in Cyber Security (CiCS)**, an NWO Gravitation project.

- **Date:** Wednesday, 27 January 2027, 12:30 – 17:30, followed by drinks
- **Location:** Vrije Universiteit Amsterdam (room to be announced)
- **Registration:** <https://cryptpad.fr/form/#/2/form/view/d-FrQ-Tqb-tQkW5K+PJRydmjYejnx3B9NAYOYdB1E+o/>
- **Registration responses:** CryptPad form owned by the organisers' CryptPad account (cryptpad.fr, end-to-end encrypted). Export via the form's *Responses* view → export as CSV; delete the form after the meeting.
- **Live page:** <https://www.challenge-cyber.nl/events/meeting-2027/>
- **Old address:** <https://cics-project.github.io/meeting-2027/> forwards to the live page. GitHub Pages publishes it from the `pages-redirect` branch, so leave that branch as it is.

## Editing

This repository (`main`) holds the source. Pushing to `main` does **not** change the live page. See [Build and deploy](#build-and-deploy).

| What to change | File |
|---|---|
| Program: sessions, times, titles, speakers, breaks | `_data/program.yml` |
| Date, time, location, registration link, project name | `_config.yml` |
| Page structure (HTML) | `index.html`, `_layouts/default.html` |
| Styling | `assets/style.css` |

In `_data/program.yml`, each item has a `time`, a `title`, an optional `detail` (e.g. speaker), and `break: true` for coffee/drinks rows.

To preview locally: run `"$(gem environment user_gemdir)/bin/jekyll" serve`, then open <http://localhost:4000/meeting-2027/>. If Jekyll is missing, install it with `gem install --user-install jekyll`.

## Build and deploy

The live page is served from the TU/e GitLab repository `git@gitlab.tue.nl:mcscc/cics.git`, checked out at `~/Gitlab/cics`. Everything in its `public/` directory goes live at <https://www.challenge-cyber.nl> within a minute of a push to `master`, so check the diff first. Don't touch `.gitlab-ci.yml` there.

1. Commit and push the source change to `main` here, then build:

   ```sh
   cd ~/Web/cics-meeting-2027
   git pull --ff-only
   "$(gem environment user_gemdir)/bin/jekyll" build
   ```

2. Copy the build into the GitLab checkout. The trailing slash on `_site/` matters, and `--delete` removes old files from this event's folder only:

   ```sh
   git -C ~/Gitlab/cics pull --ff-only
   rsync -av --delete _site/ ~/Gitlab/cics/public/events/meeting-2027/
   ```

3. Review, commit and push:

   ```sh
   cd ~/Gitlab/cics
   git status
   git diff
   git add public/events/meeting-2027
   git commit -m "Update CiCS meeting 2027 event page"
   git log -1 --format=full
   git push
   ```

4. Open <https://www.challenge-cyber.nl/events/meeting-2027/> and check the content and the styling.

**Commits must never credit Claude.** Commit messages in the GitLab repository (and this one) must not contain a `Co-Authored-By: Claude` line or any other mention of Claude. Check the output of `git log -1 --format=full` before pushing.

The stylesheet link in `_layouts/default.html` must stay relative (`assets/style.css`), because the page lives in a subdirectory.
