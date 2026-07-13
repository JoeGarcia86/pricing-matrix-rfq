# pricing-matrix-rfq

Interactive pricing/RFQ tool for warehouse customer quotes — building specs intake, regional cost benchmarks (rent/utilities/labor), margin slider showing price per pallet/order/sq ft, stored pricing history, SOW revision addendum, and Excel export.

## What's in this repo

- `pricing_tool.html` — the full tool. Single self-contained file, no build step, no dependencies to install. Open it in any browser (Chrome/Edge recommended) to run it.

## Features

- **RFQ Intake** — customer/operation type, building specs (with a spec-sheet upload that auto-detects sq ft, rent, and utility figures from text files), and monthly volume inputs (pallets, orders, lines, units).
- **Regional Benchmarks** — editable rent/utility/labor defaults by region (West Coast, Northeast, Midwest, Southwest, Southeast, Mountain, National), sourced from public industrial real estate, EIA electricity, and warehouse labor data. Includes a table to log your own vendor/facility actuals for comparison.
- **Process Time Standards** — editable minutes-per-unit assumptions (receiving, putaway, picking, packing, loading) used to estimate labor hours from volume.
- **Cost & Margin** — full cost build-up (facility, labor, overhead), a live 0–50% margin slider showing price per pallet/order/sq ft/labor hour in real time, a margin target gauge, and a directional check against published industry price ranges.
- **Pricing History** — every saved quote stored by customer + warehouse + date with full inputs and outputs, searchable, so any price can be traced back to how it was built.
- **SOW Addendum** — select a past quote, flag what changed, and generate a formatted before/after pricing addendum saved as a new revision.
- **Export** — generates a native Excel workbook (`.xls`, SpreadsheetML format) with live formulas: quote summary, cost build-up, benchmarks used, industry check, and pricing history log. Editing a cell in Excel (e.g. margin %) recalculates the price.

## How to use it

1. Open `pricing_tool.html` in a browser.
2. Fill in the RFQ Intake tab (customer, building specs, volumes).
3. Check/adjust Regional Benchmarks for the market this facility is in.
4. Go to Cost & Margin, move the slider to find the right price at the right margin.
5. Save the quote to Pricing History.
6. Export to Excel for the customer file or internal approval.

Data is stored in the browser's local storage, so history persists between sessions on the same machine/browser profile.

## Data sources for default benchmarks

Industrial rent: Statista, ReadySpaces regional market reports (2025–26).
Electricity/utility rates: U.S. Energy Information Administration (EIA), commercial/industrial rates (2026).
Warehouse labor rates: Salary.com, PayScale, C3 Solutions warehouse labor surveys (2025–26).
3PL price ranges (storage, receiving, pick/pack): The Fulfillment Advisor, industry 3PL pricing guides (2025–26).

These are directional starting points — always verify against current vendor quotes before finalizing customer pricing.
