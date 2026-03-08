# Repository Guidelines

## Project Structure & Module Organization
This repository centers on one primary artifact: the brand system file.
- `index.html`: main brand book containing HTML, CSS, and presentation sections (served at `/` by Netlify).
- `AGENTS.md`: contributor guide for future updates.

Treat the HTML file as the canonical source for brand foundations (color, typography, spacing, voice, and usage examples). Keep related changes grouped by area (for example: root variables, layout sections, and responsive rules). SVG assets live in `assets/`. If the project grows, add `css/` and `js/` directories instead of expanding inline blocks.

## Build, Test, and Development Commands
No build system is configured. Use a local static server for development:
- `python3 -m http.server 8000` - serves the repository at `http://localhost:8000`.
- `xdg-open 'http://localhost:8000'` - opens the page in a browser.

Manual validation is expected: check layout, typography, color usage, and section navigation after edits.

## Coding Style & Naming Conventions
- Use 2-space indentation in HTML/CSS blocks for consistency with the current file.
- Prefer semantic, hyphenated class names (for example: `.toc-section`, `.cover-inner`).
- Keep CSS custom properties in `:root` as the single source of truth for brand colors and fonts.
- Group styles by section using concise comment headers (for example: `/* ── COVER ── */`).
- Build brand patterns as reusable sections and avoid one-off visual overrides unless they are documented as exceptions.

When renaming classes or IDs, update all matching selectors and anchors in one change.

## Testing Guidelines
Automated tests are not set up. Before submitting changes:
- Load the page at desktop and mobile widths.
- Verify no console errors in browser DevTools.
- Confirm internal links/anchors and visual hierarchy still work.

If JavaScript or tooling is added later, include a test runner and document commands here.

## Commit & Pull Request Guidelines
Git history is not available in this directory, so no existing commit convention can be inferred. Use this baseline:
- Commit format: `type(scope): short summary` (example: `style(cover): refine hero spacing`).
- Keep commits focused on a single concern.
- PRs should include: purpose, key visual/content changes, before/after screenshots, and any follow-up tasks.
