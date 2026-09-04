# Jeremy's Desk

An interactive desktop-OS portfolio for a data entry specialist. One self-contained HTML file — no build step, no dependencies, no external images.

**Live:** enable GitHub Pages (Settings → Pages → Deploy from branch → `main` / root) and it serves at
`https://jeremyahamioje.github.io/data-entry/`

---

## What's here

| File | Purpose |
| --- | --- |
| `index.html` | The site. A complete standalone HTML document — open it directly or host it anywhere. |
| `artifact.html` | The same page as body-only markup, for hosts that supply their own `<!doctype>` / `<head>`. |

Everything is inline: CSS, JS, and every graphic (drawn as SVG). The only network requests are three Google Fonts — Space Grotesk, JetBrains Mono, and Big Shoulders Display.

## What it does

- **Boot + lock screen** — clock, loading bar, glass link pills, click to unlock
- **Desktop** — draggable, selectable icon nodes over a blueprint-gridded wallpaper; positions persist in `localStorage`
- **Four wallpaper themes** — blue, purple, green, black
- **Widget rail** — theme picker, weather, a now-playing queue, keyboard stats, credentials
- **Dock** — magnifying toolkit icons with hover labels
- **Windows** — draggable macOS-style windows for projects, about, services, notebook, shelf, résumé, certificates, recycle bin
- **Right-click desktop** — clean up, sort by name, stickers, reset positions
- **Customization** — name your cursor and give it a badge

### Two of the apps actually work

**Data cleaner** — paste a messy column and toggle eight rules: trim and collapse whitespace, fix name casing, lowercase emails, normalize phones to E.164, normalize dates to ISO 8601, drop blanks, dedupe, sort. Runs entirely in the browser; nothing is uploaded.

**10-key drill** — three modes (numeric, currency, alphanumeric) with live per-character diffing. Scores keystrokes-per-hour and accuracy the same way a batch is scored: errors against total characters.

## Content status

The four project write-ups, notebook essays, shelf, résumé and certificates are **placeholder content** — sample work, not client engagements. The projects folder carries a visible chip saying so. Before publishing this as your own portfolio:

- Replace the name and role in the lock screen, menubar, hero, and about window
- Swap the `CASES`, `NOTES`, `SHELF` and `CERTS` arrays near the top of the `<script>` block
- Wire the real email into the `[data-mail]` handler and real URLs into the `[data-noop]` links
- Replace the drawn avatar with a real photo if you'd rather

## Editing

All content lives in plain data arrays at the top of the script — `APPS`, `FILES`, `CASES`, `NOTES`, `SHELF`, `CERTS`, `TRACKS`. Editing those changes the site; the rendering code below them doesn't need to be touched.

Design tokens (colors, fonts, shadows) are CSS custom properties in the `:root` block, with per-theme overrides on `[data-theme="..."]`.

## Credit

The interaction model and layout are a study of [parinazkassemi.com](https://www.parinazkassemi.com), rebuilt from scratch for a different profession. No assets, markup, or stylesheets were copied from it.
