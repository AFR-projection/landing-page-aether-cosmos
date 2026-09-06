# Aether Cosmos — Landing Page

Marketing site for [Aether Cosmos ByAFR](https://github.com/AFR-projection/Aether-Cosmos).

Single static page, no build step, no server.

## What's here

- **Real 3D cosmos scene** — Three.js WebGL: 4600 stars across 3 parallax layers, 4 nebula clouds, a textured planet with atmosphere + ring + orbiting moon, shooting stars, cursor particle trail. Auto-falls back to a CSS gradient if WebGL is unavailable.
- **Asymmetric composition** — Hero split (text-left, system-diagram-right). Bento grid with mixed card widths instead of equal tiles. Full-bleed deploy slab with grid mask.
- **Layered type system** — Sora (display, 200/300/500), Inter (body), Geist Mono (code/labels). Three-tier hierarchy with negative letter-spacing on display sizes.
- **Concept-color mapping** — Files = emerald, Brain = cyan, MCP = violet. The same hues run through the headline gradient, the hero orbit nodes, the bento card tags, and the deploy block code.
- **Interactive knowledge graph** — SVG visualization of the Second Brain with 6 orbiting nodes, animated pulse, and live entity counts.
- **Active section indicator** — Nav tracks scroll position; current section gets a 1px accent underline.
- **Custom marquee** — Tech-stack ticker between hero and features.
- **Motion discipline** — `prefers-reduced-motion` honored: scene freezes, marquee stops, reveals snap on.

## Stack
- Pure HTML / CSS / vanilla JS
- [Three.js 0.160](https://unpkg.com/three@0.160.0/build/three.module.js) via ES module CDN
- [Sora](https://fonts.google.com/specimen/Sora) + [Inter](https://fonts.google.com/specimen/Inter) + [Geist Mono](https://fonts.google.com/specimen/Geist+Mono) (Google Fonts)

## Local preview
```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy
Drop `index.html` into any static host (GitHub Pages, Cloudflare Pages, Netlify, nginx).

## Design tokens
Pulled from the main app's design system at `AFR-projection/Aether-Cosmos/design-system/aether-cosmos-byafr-auth/MASTER.md`:
- Primary: `#1E3A5F` → adapted to a deeper ink palette (`#050608` / `#0a0d12` / `#11151c`) for cosmic feel
- Accent: emerald `#4ade80` + cyan `#22d3ee` + violet `#a78bfa` (for the 3 concept nodes)
- Typography: Sora display, Inter body, Geist Mono code
- Style: dark, cinematic, asymmetric, technical, premium
