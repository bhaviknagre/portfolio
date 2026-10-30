# Bhavik Nagre — Portfolio

Single-page, static (no build step) portfolio for an AI & Data Engineer. Dark, glassmorphic, developer-centric UI. Pure HTML5 + CSS3 + vanilla JS, [Lucide](https://lucide.dev) icons via CDN — deploys as-is to GitHub Pages.

## Run locally

Any static file server works, e.g.:

```bash
python3 -m http.server 8080
# or
npx serve .
```

Then open `http://localhost:8080`.

## Images

All images live in **`assets/img/`**:

| Item | Path | Where it's used |
|---|---|---|
| Headshot | `assets/img/profile-photo.jpg` | Hero section |
| Ollion logo | `assets/img/ollion-logo.jpeg` | Experience — both Ollion entries |
| Xscientist logo | `assets/img/xscientist-logo.jpeg` | Experience — Xscientist entry |
| Claude Certified Architect badge | `assets/img/claude-architect-badge.png` | Certifications |
| Google Cloud logo | `assets/img/google-logo.png` | Certifications |
| AlmaBetter logo | `assets/img/almabetter-logo.jpeg` | Certifications |

Each falls back to a styled icon placeholder if the file is missing, so nothing looks broken while you're adding them.

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
- [Lucide](https://unpkg.com/lucide@1.25.0/dist/umd/lucide.js) icon set via CDN (pinned version), with inline brand SVGs (GitHub/LinkedIn/YouTube — Lucide dropped brand-logo icons)
- Google Fonts: Inter + JetBrains Mono
