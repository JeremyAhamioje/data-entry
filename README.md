# Jeremy's Desk

An interactive desktop-OS portfolio for data entry and data operations work. One self-contained HTML file — no build step, no dependencies, no bundler.

**Live:** enable GitHub Pages (Settings → Pages → Deploy from branch → `root` / `/ (root)`) and it serves at
`https://jeremyahamioje.github.io/data-entry/`

The default branch is `root`.

---

## What's here

| File | Purpose |
| --- | --- |
| `index.html` | The site. A complete standalone HTML document — open it directly or host it anywhere. |
| `artifact.html` | The same page as body-only markup, for hosts that supply their own `<!doctype>` / `<head>`. |
| `portrait.jpg` | Source headshot, cropped square. Already inlined as a data URI in the HTML. |

Everything is inline: CSS, JS, the portrait, and every icon (drawn as SVG). External requests are limited to three Google Fonts and the Spotify embed.

## What it does

- **Boot + lock screen** — clock, loading bar, contact pills, click to unlock
- **Desktop** — draggable, selectable icon nodes over a blueprint-gridded wallpaper; positions persist in `localStorage`
- **Four wallpaper themes** — blue, purple, green, black
- **Widget rail** — theme picker, live Lagos clock, Upwork hours, a real Spotify player with a four-track queue, and the services list
- **Dock** — magnifying toolkit icons with hover labels
- **Windows** — draggable macOS-style windows for projects, about, what-I-do, notebook, shelf, résumé, sticky notes, and file previews
- **Floating contact dock** — email, WhatsApp, Upwork, LinkedIn and X, bottom right
- **Right-click desktop** — clean up, sort by name, stickers, reset positions

### Two of the apps actually work

**Data cleaner** — paste a messy column and toggle eight rules: trim and collapse whitespace, fix name casing, lowercase emails, normalize phones to E.164, normalize dates to ISO 8601, drop blanks, dedupe, sort. Runs entirely in the browser; nothing is uploaded.

**10-key drill** — three modes (numeric, currency, alphanumeric) with live per-character diffing, scoring the viewer's own keystrokes-per-hour and accuracy.

## Content and honesty

Every claim on the page is one that can be backed up:

- **3,000+ hours** of data work, linked to the live Upwork profile
- **Company DB** (`company-db-clone.vercel.app`) is a real, live build and is labelled as a personal build
- The other **three projects are independent samples** — each carries a visible note reading *"This is my own sample dataset, built to demonstrate the workflow. It is not a client engagement."*

There are no invented client names, no fabricated volume or accuracy figures, and no certifications listed. The notebook and résumé describe method and service areas rather than claimed results.

**Screenshots are still placeholders.** Each project has a dashed `.shot` frame saying what image belongs there. Drop real screenshots in by replacing the `shot:[title, caption]` entries in the `CASES` array with `<img>` markup.

## Editing

All content lives in plain data arrays at the top of the `<script>` block — `APPS`, `FILES`, `CASES`, `NOTES`, `SHELF`, `SKILLS`, `TRACKS`. Editing those changes the site; the rendering code below them doesn't need to be touched.

Design tokens (colors, fonts, shadows) are CSS custom properties in the `:root` block, with per-theme overrides on `[data-theme="..."]`.

To swap the music, replace the Spotify track IDs in `TRACKS`. To change the portrait, re-crop the source square and re-inline it as a base64 data URI.

## Credit

The interaction model and layout are a study of [parinazkassemi.com](https://www.parinazkassemi.com), rebuilt from scratch for a different profession. No assets, markup, or stylesheets were copied from it.
