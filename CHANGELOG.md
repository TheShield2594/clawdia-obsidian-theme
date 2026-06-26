# Changelog

## 1.3.0

- Fixed light-theme H2 heading contrast (was 2.92:1, now 5.40:1 using `--clawdia-claw-700`)
- Fixed light-theme code comment contrast (was 2.74:1, now 5.17:1 using `--clawdia-ink-600`)
- Fixed button text contrast: switched from white to `--clawdia-ink-950` on accent (now 5.98:1, was 3.15:1)
- Fixed light-theme tag colors using stale hardcoded `rgba(194, 95, 46, ...)` — now uses `rgba(var(--interactive-accent-rgb), ...)` so tags respond to Style Settings accent changes
- Replaced emoji 🐈 watermark with an inline SVG paw print that renders identically across all platforms and responds to accent color
- Added `@media (prefers-reduced-motion: reduce)` to disable button transform for users who prefer reduced motion
- Added ~38 missing Obsidian CSS variables across both themes: `--icon-color`, `--nav-item-*`, `--titlebar-*`, `--ribbon-*`, `--divider-*`, `--toggle-*`, `--vault-name-*`, `--link-decoration-*`, `--input-*`, `--drag-ghost-*`, `--embed-*-radius`, `--checklist-done-*`, `--prompt-text`, `--background-modifier-active`, `--background-modifier-message`, `--workspace-background-translucent`, `--settings-home-background`, and more
- Updated README color palette table with correct computed `color-mix()` values and added a full accent scale reference table
- Cleaned up `.gitignore` to remove overly broad `*.md` rule

## 1.2.0

- Bumped version for Obsidian community directory re-submission

## 1.1.0

- Added [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) support: customizable accent color, body font size, and toggles to hide the paw watermark or heading ornament
- Themed editor cursor and selection in live preview
- Themed left ribbon, right-click/slash-command menus, embeds (notes, images, PDFs), and frontmatter property icons
- Added mobile-specific styling for the navbar and drawer
- Fixed light-mode link/accent text contrast (was 2.9:1, now 5.6:1 against background) by introducing `--clawdia-claw-700`

## 1.0.0

- Initial release: dual light/dark themes, gothic warmth palette, custom typography, syntax highlighting, callouts, graph view, canvas support, paw watermark
