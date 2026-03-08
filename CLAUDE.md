# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Contrôle de Gestion is a brand identity system for public management control (Contrôle de Gestion Ministériel, Cameroun). The repository contains static HTML/CSS brand books and SVG logo assets — no build tools, frameworks, or test suites.

## Key Files

- `pulsera-brand-book-v10-light.html` — Main brand book (HTML + inline CSS). Canonical source for colors, typography, spacing, voice, and usage guidelines. Contains both dark and light editions.
- `v2.html` — Separate brand concept page (Tailwind CSS via CDN).
- `logo.svg` — Brand logo (piston mark, viewBox 0 0 224 295).
- `second_logo.svg` — Cameroon national emblem (raster-in-SVG, 960×1088).
- `business-card.html`, `business-card_v1.html` — Standalone business card files.
- `brand-objects.html` — Standalone brand objects file.
- `*.svg` — Other logo and symbol assets (`Frame.svg`, `SymbolContainer_margin.svg`, etc.).

## Development

No build system. Serve locally with a static server:

```
python3 -m http.server 8000
```

No automated tests. Validate manually: check layout at desktop/mobile widths, verify no console errors, confirm anchors and visual hierarchy work.

## Coding Conventions

- 2-space indentation in HTML/CSS.
- Semantic, hyphenated class names (e.g., `.toc-section`, `.cover-inner`).
- CSS custom properties in `:root` are the single source of truth for brand colors and fonts.
- Group styles by section with comment headers (e.g., `/* ── COVER ── */`).
- When renaming classes or IDs, update all matching selectors and anchors in one change.

## Brand Design Tokens (main brand book)

- **Fonts:** `--serif` (Outfit), `--sans` (Space Grotesk), `--mono` (JetBrains Mono)
- **Core palette:** `--ink` (#0a0c10), `--navy` (#1a1d23), `--blue` (#475569), `--mid`/`--steel` (#94a3b8), `--silver` (#cbd5e1), `--mist` (#e2e8f0), `--white` (#f1f5f9), `--gold` (#f97316), `--gold-lt` (#fb923c), `--gold-dk` (#ea580c)
- **Domain:** controle-gestion.cm

## Commit Convention

`type(scope): short summary` (e.g., `style(cover): refine hero spacing`). Keep commits focused on a single concern.
