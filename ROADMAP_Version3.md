# Roadmap (offline-first)

Priority: get a stable offline experience and robust export/import before adding advanced features.

## v0.1 — Offline core (1–2 weeks)
- UI for basic transactions, categories, budgets.
- IndexedDB persistence via Dexie.
- Export to XLSX and JSON.
- Import JSON and XLSX with validation.
- PWA shell (manifest + Service Worker).

## v0.2 — Reliability & UX (2–4 weeks)
- Client-side encryption for JSON backups.
- File System Access API support (optional).
- Recurrence rules for future planning.
- Monthly charts (Chart.js or Chartist).
- Export scheduling reminders (UI only).

## v0.3 — Polish & tests (3–6 weeks)
- E2E tests for import/export & PWA install.
- Accessibility audit & WCAG fixes.
- UI/UX polish and responsive layouts.

## v0.4 — Visual identity & usability
- Light/dark mode toggle and system-preference detection.
- Seven pastel themes: blue, pink, olive, beige, purple, black, white.
- UX review focused on making navigation, labels and feedback more intuitive; consolidate quick actions, improve empty states and add contextual help where needed.

## v0.5 — Income & budget flexibility
- Multiple named income sources (e.g. salary, rental, side income) each with amount, frequency and start/end dates.
- Income projections and contribution split to savings/debt/investments.

## v0.6 — Investments & debt
- Debt payment plans similar to investment projections: enter starting month, monthly payment, interest rate and fees; show amortization schedule and projected payoff date.
- Ability to add new debt at a specific point in time, increasing total debt and affecting interest calculations from that month onward.
- Investment diversification: define up to three indexes/funds with individual allocation percentages and expected returns, plus combined portfolio view.

## v0.7 — Wealth and assets
- Asset origin type: financed, inherited, acquired, each tracked with current value.
- Vehicles: enter mileage, registration date and model year; apply a depreciation model (e.g. higher initial drop, flattening over age/mileage) to estimate current value.
- Financed items: calculate estimated full-ownership date from the linked payment plan, total interest paid and residual value at transfer of ownership; for vehicles use the depreciation model, for other items allow a custom appreciation/depreciation estimate (e.g. gold +2% per year) or a fixed value.
- Wealth summary shows total, net and liquid assets at any selected date.