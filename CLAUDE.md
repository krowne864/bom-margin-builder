# Instructions for Claude

Read this file at the start of every session on this project.

## About the owner

- Goose (gdawson@krowne.com) is not a software engineer — explain things in plain English, no jargon.
- Goose edits only `README.md`, `docs/`, and `data/`. Claude owns `index.html` and `scripts/`.

## What this app is

A single-page, browser-only pricing & BOM tool. No backend, no database, no API keys.
All math runs in the page. Hosted on GitHub Pages from the repo root (`index.html`).

## Standing rules

- Apply Krowne branding (use the krowne-branding skill) to all visual output.
- The whole app is one self-contained `index.html` (inline CSS + JS). Keep it that way unless it grows enough to warrant splitting.
- Before large changes, summarize the plan in one or two sentences and confirm.
- Never delete files without asking.
- After UI changes, verify visually (screenshot via Chrome tools when available).
- Update `README.md` ("How to run it") whenever setup steps change.

## Pricing logic (do not change without confirming)

- List price = (cost × markup) / 0.45
- Freight is always added to loaded cost (no automatic waiving).
- "Markup as dependent variable" mode: user enters Cost and List directly; markup = (list × 0.45) / cost, shown as a computed number not limited to the 1.0–3.0 slider range. Use for existing items with a published list and known cost.
- Dealer-net factors by discount tier are defined in the `TIERS` array in `index.html`.
- Item margin = (dealer net − loaded cost) / dealer net.
- Gross margin (project, blended) = (total dealer net − total loaded cost) / total dealer net.
- "Set markup for all" and "Set tier for all" bulk-apply a common markup / discount tier to every BOM line.
- The BOM shows freight per line.

## Deploy

GitHub repo `krowne864/bom-margin-builder` → GitHub Pages (Deploy from `main`, root).
Push to `main` and Pages redeploys automatically.

## Project-specific notes

(Claude: add decisions and gotchas here as the project evolves.)
