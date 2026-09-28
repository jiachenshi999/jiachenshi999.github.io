# Jiachen Shi academic homepage

This is a static academic homepage, published at <https://jiachenshi999.github.io/> from the public [GitHub repository](https://github.com/jiachenshi999/jiachenshi999.github.io). It needs no paid hosting, database, package install, or build step.

For the optional free Cloudflare Pages deployment and shared `.com` subdomain setup, see [CLOUDFLARE_DEPLOY.md](CLOUDFLARE_DEPLOY.md). Cloudflare deployment is pending account setup; the existing GitHub Pages site remains live.

## Edit the site

- **Biography, appointments, projects, and paper text:** edit `index.html`. Each section has an `id` such as `research` or `publications`.
- **Colors and layout:** edit `styles.css` (the palette is defined at the start of the file).
- **Portrait:** replace `assets/jiachen-shi.jpg` with a new image of the same name. The original source photo is kept locally and excluded from Git.
- **New section:** copy a `<section>` block in `index.html`, give it a unique `id`, and add a matching link in `<nav class="site-nav">`.
- **Paper link:** use a verified DOI URL (`https://doi.org/...`) on its title. Add `target="_blank" rel="noopener noreferrer"` if it opens a new tab.

Open `index.html` directly to preview most changes, or run `python -m http.server 8000` in this folder and visit `http://localhost:8000/`. The site uses relative asset paths, so it also works from a GitHub project repository path.

## Publish updates

The GitHub repository is already live. Changes committed to its `main` branch appear on the public site automatically. You can edit a text file directly on GitHub, or ask Codex to update this folder and publish the corresponding files.

For a Git-linked working copy on another computer, clone the repository:

```powershell
git clone https://github.com/jiachenshi999/jiachenshi999.github.io.git
```

Make future edits inside that clone, then run `git add`, `git commit`, and `git push`. This original project folder is a source snapshot, not a Git checkout. If you edit here, copy only the website files into the clone before committing. The source CV (`个人简历.docx`) and original photo (`ETH+22-01-1037.jpg`) must stay out of the public repository; `.gitignore` lists both.

## Content notes

The profile was drafted from `个人简历.docx` in September 2026. It intentionally omits birth details and does not publish the full CV file. Publication and project translations should be reviewed by Jiachen Shi before treating them as a formal record. The visible paper links were checked against DOI or publisher records.

