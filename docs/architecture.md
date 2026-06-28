# Architecture (plain English)

This app is intentionally simple: **one file, no backend.**

```
Browser
   │
   ▼
index.html   ← the entire app: HTML layout + inline CSS + inline JavaScript
```

- All pricing math (list, dealer net, margin, effective margin) runs in JavaScript in the page.
- Discount tiers and their dealer-net factors are defined in the `TIERS` array.
- No external calls except loading the Jost web font from Google Fonts.
- No data is saved — refreshing the page clears the BOM. CSV export is how you keep a copy.

## Hosting

GitHub Pages serves `index.html` from the repo root. A `.nojekyll` file is included so
Pages serves the files as-is without Jekyll processing. Pushing to `main` redeploys.

## Why it diverges from the template's server layout

The Krowne `_template` includes `server/` folders for apps that need a backend,
integrations, or a database. This tool needs none of that, so those folders are omitted.
If the app ever needs to pull live cost data (e.g. from Business Central), add a
`server/integrations/business-central/` folder per the template and route the UI through
`server/api` — never call external systems directly from the page.
