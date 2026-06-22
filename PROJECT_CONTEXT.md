# MD → Anki

Client-only web tool that converts Markdown (especially from AI chatbots) into per-section PNG images, ready for Anki cards.

أداة ويب لتحويل نصوص Markdown إلى صور PNG منفصلة لكل قسم، جاهزة للصق في بطاقات Anki.

## Stack
- TanStack Start v1 + React 19 + Vite 7
- The app itself is a single self-contained file: `public/md-anki.html`
- All libraries (KaTeX, marked, html2canvas, highlight.js) live in `public/vendor/` — no CDN

## Architecture
- `src/routes/index.tsx` mounts `public/md-anki.html` in a fullscreen `<iframe>`.
- `public/md-anki.html` contains all HTML + CSS + JS for the app.

## Features
- Live Markdown preview with KaTeX math
- Editor / Split / Preview modes
- Per-section PNG export via html2canvas
- Arrow rendering with bidi isolation for Arabic
- Light/Dark theme + settings (font size, line height, export scale)
- LocalStorage drafts + settings persistence
