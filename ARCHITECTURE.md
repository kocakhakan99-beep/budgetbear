# Architecture

## Principles

- The app runs client-side with no application server.
- Data is stored in the user's browser (`localStorage`).
- Data portability is achieved through explicit exports (XLSX, PDF, and JSON).
- The JSON export is the lossless backup format.

## Core components

- UI: vanilla HTML and JavaScript for budgets, investments, debts, and assets.
- Persistence: `localStorage` state managed by `src/js/app.js`.
- Export/import: SheetJS for Excel, jsPDF for PDF, and JSON serialization for
  backups.
- Calculation layer: budget projections, investment growth, debt amortization,
  and net-worth summaries.

## Persisted state

- `settings`: plan dates, income, portfolio values, and display preferences
- `categories`: expense and income categories with archive state
- `budgets`: amount, type, category, frequency, and validity period
- `debts`: balance, payment, interest, fees, and start month
- `assets`: type, name, value, liability, cost, and start month

Keep state migrations in `src/js/app.js` whenever the persisted shape changes.
Do not store user exports or other private files in the repository.

## Export and restore

- XLSX and PDF are reporting formats for sharing or analysis.
- JSON is the lossless restore format.
- JSON imports are migrated before replacing the current in-memory state.
- Excel import supports the application's MASTER workbook format.
