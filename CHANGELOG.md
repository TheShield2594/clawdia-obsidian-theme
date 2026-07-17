# Changelog

## 1.3.1

- **Fixed broken callout colors**: Obsidian consumes callout type colors as RGB triplets inside `rgba()`, so the previous hex/`var()` values were invalid and callouts fell back to Obsidian defaults. All 14 callout variables are now proper RGB triplets in both themes
- Renamed `--callout-danger` (not a real Obsidian variable) to `--callout-error`, and added the previously missing types: `todo`, `summary`, `important`, `fail`, `bug`, `example`
- **Fixed no-op table variables**: `--table-header-border`, `--table-column-first-border`, `--table-column-last-border`, and `--table-row-last-border` don't exist in Obsidian — replaced with the real `--table-header-border-width`/`--table-header-border-color` and `-width`-suffixed variables
- **Blockquotes now themed in Live Preview**: switched from element-only `blockquote` rules to Obsidian's `--blockquote-*` variables, which cover both reading view and the editor
- **Accent color now fully cascades**: replaced 37 hardcoded `rgba(217, 119, 66, …)` / `rgba(var(--interactive-accent-rgb), …)` tints with `color-mix()` derived from `--clawdia-claw-500`, so changing the accent in Style Settings updates hovers, selections, highlights, tag chips, the watermark, and button shadows (note: `--interactive-accent-rgb` itself remains static, as CSS cannot derive an RGB triplet from a variable)
- Light-mode contrast fixes (WCAG AA): vault name and property keys `claw-500` (2.92:1) → `claw-700` (5.40:1); code `function`/`tag`/`value`/`important` tokens → `claw-700` on a lightened `cream-100` code background (4.94:1); `--text-warning` → `#8a5d0c` (5.34:1); external link hover → new `moss-600` (6.04:1); active icon states → `claw-600`
- Light-mode `mark` highlights now match dark mode's border radius and padding
- README: corrected the scrollbar feature claim (no Firefox-specific styling existed, and Obsidian is Chromium-based)

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
