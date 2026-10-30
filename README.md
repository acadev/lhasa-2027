# LHASA 2027 — workshop website

Static site for **Scaling Long-Horizon Agentic AI Systems for Scientific Discovery (LHASA)**, a workshop proposed for SupercomputingAsia 2027 (1–4 March 2027, Singapore).

Single file, no build step, no dependencies. `index.html` is the whole site.

## Publishing on GitHub Pages

You need a GitHub account. Two options for the URL:

### Option A — project site: `https://<username>.github.io/lhasa-2027/`

1. Create a new public repository named `lhasa-2027`.
2. Upload `index.html` to the repository root (web UI: **Add file → Upload files**), or from the terminal:
   ```bash
   git init
   git add index.html README.md
   git commit -m "LHASA 2027 workshop site"
   git branch -M main
   git remote add origin https://github.com/<username>/lhasa-2027.git
   git push -u origin main
   ```
3. In the repository, go to **Settings → Pages**. Under *Build and deployment*, set **Source: Deploy from a branch**, **Branch: `main`**, folder **`/ (root)`**. Save.
4. Wait about a minute, then load `https://<username>.github.io/lhasa-2027/`.

### Option B — user site: `https://<username>.github.io/`

Same steps, but name the repository exactly `<username>.github.io`. This claims your account's root GitHub Pages URL, so use it only if you don't want it for something else.

### Custom domain (optional)

If you have a domain such as `lhasa-workshop.org`, add it under **Settings → Pages → Custom domain**, then create a CNAME record at your DNS provider pointing to `<username>.github.io`. GitHub writes a `CNAME` file into the repository automatically.

## Editing

Everything is in `index.html`:

- Colors and fonts: the `:root` block at the top of `<style>` (and the two dark-theme blocks below it).
- Dates: the `#submit` section, inside `.dates`. Keep the `datetime` attributes in ISO form.
- Topics: the `#topics` grid — add or remove a `<div class="topic">`.
- People: `#organizers` and `#pc`.
- Contact address: the `#contact` section (`<span class="mailbox">`).

Commit and push; Pages redeploys within a minute.

## Still to fill in

- Submission link (Linklings URL) once the conference opens the track.
- The confirmed workshop day (1 or 4 March).
- Confirmed keynote speakers, panelists, and remaining program committee members.
- Proceedings venue, once the conference confirms the arrangement.
