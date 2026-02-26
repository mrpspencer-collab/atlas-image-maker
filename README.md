# Atlas Post Creator

A self-contained visual post creator for the Atlas BI platform, used by Audi dealership analysts to turn AI-detected data anomalies into shareable newsfeed posts for GMs and internet managers.

## What it does

**Human-in-the-loop workflow:**
1. Atlas AI detects a KPI anomaly (e.g. VDP Views +47%)
2. Analyst opens the Post Creator and designs a visual around the insight
3. Post publishes to the Atlas newsfeed as an Instagram-style card

## Features

- **Format picker** — Square (newsfeed thumbnail), Landscape (post header), Portrait, Standard, Banner, Poster
- **Layered editor** — drag, resize, and reorder text, image, and shape layers
- **Text presets** — Headline, KPI Value, Subheading, CTA, Label with pre-configured styles
- **Background images** — 20 procedurally generated scenes (mountains, city, abstract, automotive, etc.) or upload your own
- **Uploaded image pan** — drag to reposition a background photo after uploading
- **15 templates** — from clean data-viz layouts to editorial magazine covers, punk zines, synthwave, brutalist, automotive
- **Proportional rescaling** — switching formats rescales all layers and fonts intelligently
- **Off-canvas recovery** — layers outside the canvas are flagged in the panel with a one-click snap-back button
- **Integrated flow** — "Image creator" CTA inside the Create a Post modal; finished image returns as a thumbnail

## Files

| File | Description |
|------|-------------|
| `index.html` | Full integrated flow — Create a Post modal + Image Creator |
| `editor.html` | Standalone image editor only |

## Deployment

**No build step required.** Both files are fully self-contained — all dependencies load from CDN.

### Netlify
Drag and drop this entire folder onto [netlify.com/drop](https://app.netlify.com/drop).

### FTP / any static host
Upload `index.html` (and optionally `editor.html`) to any directory on your server.

### GitHub Pages
1. Push this repo to GitHub
2. Go to **Settings → Pages → Source → main branch / root**
3. Your app will be live at `https://yourusername.github.io/atlas-post-creator/`

## Tech

- React 18 via CDN (no build step)
- Babel standalone for JSX transpilation
- html2canvas for canvas-to-JPEG export
- All imagery generated procedurally with HTML Canvas API — no external image URLs
