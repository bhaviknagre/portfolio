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

All images live in **`assets/img/`** — that's the folder to drop your files into. Use these exact filenames and they'll appear automatically (each one currently falls back to a clean styled icon placeholder, so nothing looks broken in the meantime):

| Item | Path to add | Where it's used |
|---|---|---|
| Your headshot | `assets/img/profile-photo.jpg` | Hero section |
| Ollion logo | `assets/img/ollion-logo.png` | Experience — both Ollion entries |
| Xscientist logo | `assets/img/xscientist-logo.png` | Experience — Xscientist entry |
| Google Cloud logo | `assets/img/google-logo.png` | Certifications |
| AlmaBetter logo | `assets/img/almabetter-logo.png` | Certifications |
| YouTube walkthrough link | `index.html` → search `Watch Walkthrough` | DocuMind project card currently points to `#` (placeholder) |

## Structure

```
index.html          All markup/content
style.css           All styling (CSS variables at the top control the theme)
script.js           Nav toggle, scroll-reveal animations, active-link highlighting, back-to-top
assets/img/         Drop your photo + company/cert logos here (see table above)
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
