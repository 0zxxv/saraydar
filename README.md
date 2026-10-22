# Abuquwa Villas — Project Control System

Saraydar Real Estate · exported 22 Oct 2026

## Contents

| File | What it is |
| --- | --- |
| `index.html` | The full system: interface, Saraydar theme and all logic in one file |
| `data/all-data.json` | Every record in the system, grouped by section |
| `data/tasks.json` | Schedule: 36 tasks across 7 phases and the sales track |
| `data/costs.json` | Budget lines |
| `data/payments.json` | Payments, each linked to a cost line by `costId` |
| `data/units.json` | The 4 villas: status, price, buyer, amount collected |
| `data/risks.json` | Risk register |
| `data/log.json` | Site log entries |
| `data/meta.json` | Project name, developer, start and target handover dates |

## Important: how the data works

On Netlify or any static host, `index.html` loads the starting records from
`data/all-data.json` and keeps edits in the browser (`localStorage`).
On Claude, it still uses Claude's built-in database when that API is present.

Everything else (views, calculations, forms, theme) works as is.

## Data notes

- Amounts are in Bahraini dinars (BD), stored as plain numbers.
- Dates are ISO strings (`YYYY-MM-DD`).
- The land payment has no date recorded yet.
