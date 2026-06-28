# BOM Margin Builder

**What it is:** A Krowne-branded pricing tool that turns part cost + markup into list price, dealer net (by discount tier), and margin — then rolls multiple line items into a Bill of Materials with a blended "effective margin." Includes CSV import/export and an email-summary button.

**Status:** Working

**How to run it:** It's a single static page. Open `index.html` in any browser, or use the hosted GitHub Pages URL (see below). No build step, no server, no keys.

## Live URL

Hosted on GitHub Pages from the repo root. Repo: `krowne864/bom-margin-builder`.
Once Pages is enabled (Settings → Pages → Deploy from `main` / root), the URL is:
`https://krowne864.github.io/bom-margin-builder/`

## Quick links

- What it should do → `docs/requirements.md`
- How it's wired together → `docs/architecture.md`
- Instructions for Claude → `CLAUDE.md`

## Notes on structure

Built from the Krowne app `_template`. Because this is a single static page hosted on
GitHub Pages (which serves from the repo root), the live file is `index.html` at the
root rather than `app/pages/`. The backend folders (`server/`) the template includes
are not used — this tool runs entirely in the browser.
