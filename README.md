# Bhavik Nagre — Portfolio

Single-page, static (no build step) portfolio for a Senior AI & Data Engineer. Dark, glassmorphic, developer-centric UI. Pure HTML5 + CSS3 + vanilla JS, [Lucide](https://lucide.dev) icons via CDN — deploys as-is to GitHub Pages.

## Run locally

Any static file server works, e.g.:

```bash
python3 -m http.server 8080
# or
npx serve .
```

Then open `http://localhost:8080`.

## ⚠️ Things you still need to add before this looks fully finished

| Item | Expected filename | Where it's used |
|---|---|---|
| Your headshot | `profile-photo.jpg` (place in repo root) | Hero section — shows a styled placeholder icon until this file exists |
| Ollion logo | `company-logo-placeholder.png` | Experience — both Ollion entries |
| Xscientist logo | `company-logo-placeholder.png` | Experience — Xscientist entry |
| Google Cloud logo | `google-logo-placeholder.png` | Certifications |
| AlmaBetter logo | `almabetter-logo-placeholder.png` | Certifications |
| YouTube walkthrough link | `index.html` → search `Watch Walkthrough` | Project 1 card currently points to `#` (placeholder) |

All of the above degrade gracefully (a styled icon placeholder is shown instead of a broken image) so the site looks correct even before you add the real files — just drop the images into the repo root with the exact filenames above and they'll appear automatically.

> Note: the three experience entries all currently reference the same `company-logo-placeholder.png`. If you want distinct logos per company, add separate image files and update the `src` attributes in `index.html` for the Ollion and Xscientist `<article>` blocks under `#experience`.

## Structure

```
index.html      All markup/content
style.css       All styling (CSS variables at the top control the theme)
script.js       Nav toggle, scroll-reveal animations, active-link highlighting, back-to-top
```

## Deployment (GitHub Pages)

This repo is set up to be served directly — no build step. Once pushed to GitHub:

1. Go to **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: `main`, folder: `/ (root)`
4. Save — the site will be live at `https://bhaviknagre.github.io/portfolio/`

## Tech

- HTML5 / CSS3 (custom properties, grid, flexbox, `IntersectionObserver`-driven reveal animations)
- Vanilla JS (no framework, no build tooling)
- [Lucide](https://unpkg.com/lucide@latest/dist/umd/lucide.js) icon set via CDN
- Google Fonts: Inter + JetBrains Mono
