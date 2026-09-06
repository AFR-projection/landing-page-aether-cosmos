# Aether Cosmos — Landing Page

Marketing site for [Aether Cosmos ByAFR](https://github.com/AFR-projection/Aether-Cosmos).

Single static page, no build step, no server.

## What's here
- **Real 3D cosmos scene** — Three.js WebGL: 4600 stars across 3 parallax layers, 4 nebula clouds, a textured planet with atmosphere, ring, and orbiting moon, occasional shooting stars, and cursor particle trail. Auto-falls back to a CSS gradient if WebGL is unavailable.
- **Reduced-motion friendly** — animation is suppressed and the scene freezes when `prefers-reduced-motion` is set.
- **Performance** — DPR capped at 2, additive blending, all geometry disposed on tear-down, single requestAnimationFrame loop, no per-frame allocations.

## Stack
- Pure HTML / CSS / vanilla JS
- [Three.js 0.160](https://unpkg.com/three@0.160.0/build/three.module.js) via ES module CDN
- Inter + Space Grotesk + JetBrains Mono (Google Fonts)
- Tailwind-style utility classes inlined (no Tailwind runtime)

## Local preview
```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy
Drop `index.html` into any static host:
- **GitHub Pages** — enable Pages on the repo, branch `main`, root `/`
- **Cloudflare Pages** — connect repo, no build command
- **Netlify** — drag the folder onto the dashboard
- **Any nginx** — `cp index.html /var/www/html/`

## Design tokens
Pulled from the main app's design system at `AFR-projection/Aether-Cosmos/design-system/aether-cosmos-byafr-auth/MASTER.md`:
- Primary: `#1E3A5F`
- Accent: `#059669` / `#10b981`
- Background: `#020617`
- Font: Inter (body), Space Grotesk (headings), JetBrains Mono (code)
- Style: dark, cinematic, glassmorphism, ambient glow
