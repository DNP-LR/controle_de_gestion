# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

PULSERA is a brand identity system. The repository contains static HTML/CSS brand books and SVG logo assets — no build tools, frameworks, or test suites.

## Key Files

- `pulsera-brand-book-v10-light.html` — Main brand book (HTML + inline CSS). Canonical source for colors, typography, spacing, voice, and usage guidelines.
- `v2.html` — Separate brand concept page (Tailwind CSS via CDN).
- `*.svg` — Logo and symbol assets (`logo.svg`, `Frame.svg`, `SymbolContainer_margin.svg`, etc.).
- `AGENTS.md` — Contributor guidelines for future updates.

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

- **Fonts:** `--serif` (Playfair Display), `--sans` (Inter), `--mono` (Courier New)
- **Core palette:** `--ink` (dark slate), `--navy`/`--blue`/`--mid` (teal range), `--steel`/`--silver`/`--mist`/`--white` (light range), `--gold`/`--gold-lt`/`--gold-dk` (warm accents), `--terracotta`, `--amber`, `--parchment`

## Commit Convention

`type(scope): short summary` (e.g., `style(cover): refine hero spacing`). Keep commits focused on a single concern.
