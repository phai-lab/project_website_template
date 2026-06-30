# PHAI Lab — Paper Project-Page Template

A reusable, consistent website template for PHAI Lab paper pages, modeled on the
[UMI](https://umi-gripper.github.io/) and
[Diffusion Policy](https://diffusion-policy.cs.columbia.edu/) project pages
(both built on the [HTML5 UP **Strata**](https://html5up.net/strata) theme).

**Live demo:** https://phai-lab.github.io/project_website_template/

slate-blue default · single-variable re-theming · responsive · GitHub-Pages-ready

---

## What's here

| File / folder | Purpose |
| --- | --- |
| `index.html` | **Filled-in example** page — what a finished paper page looks like. |
| `template.html` | **Blank scaffold** — copy this to start a new page. Every section is marked with `<!-- ===== … ===== -->` comments and `REPLACE` markers. |
| `assets/css/main.css` | The Strata theme (don't edit). |
| `assets/css/phai.css` | **PHAI customizations** — change the accent color and layout tweaks here. |
| `assets/css/font-awesome.min.css`, `assets/fonts/` | Icons used in the link buttons. |
| `assets/js/` | Theme scripts (jQuery, skel, poptrox lightbox). |
| `images/` | `logo-phai.png` (favicon/logo) + `placeholder-*.svg` for every section. |
| `videos/` | Put your `.mp4` clips here. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is (no Jekyll processing). |

---

## Quick start — make a new paper page

```bash
cp template.html my-paper.html      # or edit index.html to make it the site's home page
```

Then open the copy and:

1. Search for **`REPLACE`** and fill in every spot (title, authors, abstract, BibTeX…).
2. Put figures in `images/` and clips in `videos/`, then update the `src="…"` paths.
3. Delete any section block you don't need (each is wrapped in `<!-- ===== … ===== -->`).

### Re-theme the accent color (one line)

Open `assets/css/phai.css` and change:

```css
:root { --accent: #4e79a7; }   /* slate blue (default) */
```

Examples: `#500000` maroon · `#8C1515` cardinal · `#1a73e8` blue. The title, link
buttons, author hovers, and footer all follow `--accent`.

---

## Sections included

Affiliation logos · Title / subtitle / venue · Authors + affiliations ·
Link buttons (Paper / arXiv / Code / Video / Data) · Teaser (image *or* video) ·
Abstract · Video (responsive YouTube embed) · Method (figures + text) ·
Results (responsive grid) · Team (circular author photos) · BibTeX ·
Acknowledgements · Footer.

### Link-button icons

Buttons use Font Awesome 4 via the theme's icon class. Pattern:

```html
<a href="URL" class="button special icon fa-github">Code</a>
```

Handy icons: `fa-file-pdf-o` (paper), `fa-file-text-o` (arXiv), `fa-github` (code),
`fa-youtube-play` (video), `fa-database` (data), `fa-external-link` (project).

### The results / media grid

Layout uses Strata's 12-column grid inside a `.row`. The **last** cell in a row ends
with `$`:

```
6u  + 6u$            → 2 across
4u  + 4u + 4u$       → 3 across
3u  + 3u + 3u + 3u$  → 4 across
```

---

## Preview locally

```bash
python3 -m http.server 8000
# then open http://localhost:8000   (index.html) or http://localhost:8000/template.html
```

Use a local server (not `file://`) so the relative asset paths and scripts load
correctly.

---

## Deploy on GitHub Pages

This repo is already structured for Pages (static files at the repo root + `.nojekyll`).

1. Push to GitHub (`main` branch).
2. Repo **Settings → Pages**.
3. **Source:** *Deploy from a branch* → **Branch:** `main` → **Folder:** `/ (root)` → **Save**.
4. After a minute the site is live at:
   `https://phai-lab.github.io/project_website_template/`

> For a **dedicated paper page** with its own URL, create a new repo (e.g.
> `phai-lab/my-paper`), copy this template into it, and it will publish at
> `https://phai-lab.github.io/my-paper/`. Because all asset paths are **relative**,
> it works at any sub-path with no changes.

---

## Credits

Template adapted from [HTML5 UP — Strata](https://html5up.net/strata) by @ajlkn,
free under the [CCA 3.0 license](https://html5up.net/license). Layout inspired by the
[UMI](https://umi-gripper.github.io/) and
[Diffusion Policy](https://diffusion-policy.cs.columbia.edu/) project pages.
