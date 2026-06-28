# Data

Sample/test data for the app (e.g. an example BOM CSV to import). Never hard-code
data into `index.html`.

## CSV import format

The importer matches columns by header name (case-insensitive). Recognized headers:

- Part Number (or `partnumber`, `part no`, `part#`, `sku`)
- Description (or `desc`)
- Cost
- Markup
- Freight
- Tier (or `discount tier`, `discount`)
- Qty (or `quantity`, `qoh`, `count`)

A row is imported if it has a Cost or a Part Number. Missing markup defaults to 1.7×;
an unrecognized tier defaults to 50/10.
