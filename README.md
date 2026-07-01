# PHAI Lab — Paper Project-Page Template

A reusable, consistent, and premium-looking website template for PHAI Lab paper
pages, built on the [HTML5 UP **Strata**](https://html5up.net/strata) theme.

**Live demo:** https://phai-lab.github.io/project_website_template/

PHAI-navy default · single-variable re-theming · responsive · accessible · GitHub-Pages-ready

---

## What's here

| File / folder | Purpose |
| --- | --- |
| `index.html` | **Filled-in example** page — what a finished paper page looks like. |
| `template.html` | **Blank scaffold** — copy this to start a new page. Every section is marked with `===== … =====` comments and `REPLACE` markers. |
| `assets/css/main.css` | The Strata theme (don't edit). |
| `assets/css/phai.css` | **PHAI customizations** — change the accent color and all layout tweaks here. |
| `assets/css/font-awesome.min.css`, `assets/fonts/` | Icons used in the link buttons. |
| `assets/js/` | Theme scripts (jQuery, skel, poptrox lightbox). |
| `images/` | `tamu-logo.png` (affiliation logo in the top row), `favicon.png` (browser-tab icon), `og-card.png` (social-share preview, 1200×630), and `placeholder-{teaser,thumbnail,figure,author,logo}.svg` for the teaser, paper thumbnail, and section figures. Swap these for your own assets. |
| `videos/` | Put your `.mp4` clips here. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is (no Jekyll processing). |

---

## Quick start — make a new paper page

```bash
cp template.html my-paper.html      # or edit index.html to make it the site's home page
```

Then open the copy and:

1. Search for **`REPLACE`** and fill in every spot (title, authors, abstract, BibTeX,
   and the `og:url` / `canonical` / `og:image` URLs in `<head>`).
2. Put figures in `images/` and clips in `videos/`, then update the `src="…"` paths.
3. Delete any section block you don't need (each is wrapped in `===== … =====` comments).

### Re-theme the accent color (one line)

Open `assets/css/phai.css` and change `--accent` (and the matching `--accent-rgb`):

```css
:root { --accent: #254669; --accent-rgb: 37, 70, 105; }   /* PHAI navy (default) */
```

Examples: `#500000` maroon · `#8C1515` cardinal · `#1a73e8` blue. The title, section
underlines, primary button, links, and accents all follow `--accent`.

---

## Sections included

The layout follows a well-developed robotics project-page structure:

Affiliation logos · Title / subtitle · Labeled teaser grid · Abstract ·
Paper (venue · arXiv/PDF links · clickable thumbnail) · Code & Data (icon grid) ·
Team (circular author photos + affiliation legend) · BibTeX ·
Method (figures + text) · Results (grid · side-by-side **Ours vs Baseline** comparison · quantitative table) ·
Video (responsive YouTube embed) · Acknowledgements · Contact · Footer.

### Link icons (the Code & Data grid)

The Code & Data row uses circular icon badges (Font Awesome 4):

```html
<a href="URL"><span class="ic icon fa-github"></span>Code</a>
```

Handy icons: `fa-github` (code), `fa-youtube-play` (video), `fa-database` (data),
`fa-external-link` (project), `fa-file-pdf-o` (PDF), `fa-book` (docs).
(A pill-button style — `class="button special icon fa-…"` — is also available if you prefer.)

### The results / media grid

Layout uses Strata's 12-column grid inside a `.row`. The **last** cell in a row ends
with `$`:

```
6u  + 6u$            → 2 across
4u  + 4u + 4u$       → 3 across
3u  + 3u + 3u + 3u$  → 4 across
```

On phones the result grid stacks and the team grid drops to 2-up automatically.

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
> `https://phai-lab.github.io/my-paper/`. All asset paths are **relative**, so it works
> at any sub-path with no changes — but remember to set the absolute `og:url` /
> `canonical` / `og:image` URLs in `<head>` to the new address.

---

## Credits

Template built on [HTML5 UP — Strata](https://html5up.net/strata) by @ajlkn,
free under the [CCA 3.0 license](https://html5up.net/license).
