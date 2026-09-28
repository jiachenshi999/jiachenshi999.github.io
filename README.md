# Jiachen Shi academic homepage

This is a static academic homepage. It needs no paid hosting, database, package install, or build step. The public site can live at `https://jiachenshi999.github.io/` when this folder is published from the `jiachenshi999.github.io` repository on GitHub Pages.

## Edit the site

- **Biography, appointments, projects, and paper text:** edit `index.html`. Each section has an `id` such as `research` or `publications`.
- **Colors and layout:** edit `styles.css` (the palette is defined at the start of the file).
- **Portrait:** replace `assets/jiachen-shi.jpg` with a new image of the same name. The original source photo is kept locally and excluded from Git.
- **New section:** copy a `<section>` block in `index.html`, give it a unique `id`, and add a matching link in `<nav class="site-nav">`.
- **Paper link:** use a verified DOI URL (`https://doi.org/...`) on its title. Add `target="_blank" rel="noopener noreferrer"` if it opens a new tab.

Open `index.html` directly to preview most changes, or run `python -m http.server 8000` in this folder and visit `http://localhost:8000/`. The site uses relative asset paths, so it also works from a GitHub project repository path.

## Publish free with GitHub Pages

1. Sign in to the GitHub account `jiachenshi999` and create a **public** repository named exactly `jiachenshi999.github.io`.
2. Open PowerShell in this folder and run the commands below. GitHub may ask you to sign in. The source CV (`个人简历.docx`) and original photo are in `.gitignore`; the explicit `git add` list also keeps them out of the public repository.

   ```powershell
   git init -b main
   git add .gitignore .nojekyll README.md index.html styles.css script.js favicon.svg robots.txt sitemap.xml assets/jiachen-shi.jpg
   git commit -m "Launch academic homepage"
   git remote add origin https://github.com/jiachenshi999/jiachenshi999.github.io.git
   git push -u origin main
   ```
3. In the repository, open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, then **main** and **/(root)**; save.
4. After GitHub finishes publishing, check `https://jiachenshi999.github.io/`. Future pushes to `main` update the page automatically.

If that exact repository name is unavailable, a regular public repository also works. Its URL will be `https://jiachenshi999.github.io/REPOSITORY-NAME/`.

## Content notes

The profile was drafted from `个人简历.docx` in September 2026. It intentionally omits birth details and does not publish the full CV file. Publication and project translations should be reviewed by Jiachen Shi before treating them as a formal record. The visible paper links were checked against DOI or publisher records.

