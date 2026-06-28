# Requirements (plain English)

## Goal

Help sales/engineering price a project quickly and see the margin before quoting.

## Item calculator

- Enter a part number, description, and either **cost** or **list price** (toggle).
- Pick a markup (slider, 1.0×–3.0×) and a discount tier.
- Shows list price, loaded cost, dealer net, and item margin live.
- Shows a reference table of dealer net + margin across every discount tier.
- Freight is auto-waived when cost is over $2,500.

## Bill of Materials

- Add calculated items to a running BOM with quantities.
- Edit or remove any line; change quantity inline.
- "Set tier for all" applies one discount tier to every line.
- Totals: total list, total dealer net, total loaded cost, and a blended **effective margin**.

## Import / export / share

- Import a CSV of parts (flexible column names).
- Export the BOM to CSV.
- "Email Summary" opens the mail client with a text summary of the BOM.

## Constraints

- Runs entirely in the browser — no login, no server, no stored data between sessions.
- Krowne branding (teal #01A79D, dark/light theme toggle).
