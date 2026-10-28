# Yeongwook Yang — Lab / Personal Academic Site

Static site (plain HTML/CSS, no build step) ready for GitHub Pages.

## Structure

```
index.html          Home page (bio, research interests, recent publications, contact)
journals.html       Journal articles / preprints, grouped by year, 2019 onward
conferences.html    Conference papers, grouped by year, 2019 onward
css/style.css        All styling
assets/               Put a profile photo here (e.g. assets/profile.jpg)
```

## Preview locally

Just open `index.html` in a browser, or serve it:

```bash
cd "my lab"
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy to GitHub Pages

**Option A — user/org site (recommended, URL: `https://<username>.github.io`)**

```bash
cd "my lab"
git init
git add .
git commit -m "Initial lab site"
git branch -M main
git remote add origin https://github.com/<username>/<username>.github.io.git
git push -u origin main
```

Create the empty repo named exactly `<username>.github.io` on GitHub first (Settings → General → the repo name must match your username). Pages is enabled automatically for this repo type and will be live at `https://<username>.github.io` within a minute or two.

**Option B — project site (URL: `https://<username>.github.io/<repo-name>`)**

Push to any repo, then go to the repo's **Settings → Pages**, set:
- Source: `Deploy from a branch`
- Branch: `main` / `(root)`

Save, then the site publishes at `https://<username>.github.io/<repo-name>`.

## Things to customize

- **Photo**: `assets/profile.png` (background removed, transparent PNG).
- **Lab name**: currently branded generically as "Yeongwook Yang Lab" — change the `<div class="brand">` text and page `<title>` in both HTML files if you have an official lab name.
- **Publications**: `journals.html` and `conferences.html` were generated from 총괄연구업적현황 (research record spreadsheet), limited to the last eight years (2019–2026). Own name is shown in bold; `*` marks papers where Yeongwook Yang is a main author (first or corresponding).
- **Contact section**: edit email/affiliation cards in `index.html` under `#contact`.
