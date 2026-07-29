# Roadmap (offline-first)

Priority: get a stable offline experience and robust export/import before adding advanced features.

## v0.1 — Offline core (1–2 weeks)
- [x] UI for basic transactions, categories, budgets.
- [x] Reliable browser-local persistence.
- [x] Export to XLSX and JSON.
- [x] Import JSON and XLSX with validation.
- [x] PWA shell (manifest + Service Worker).

## v0.2 — Reliability & UX (2–4 weeks)
- [x] Client-side encryption for JSON backups (AES-256-GCM, PBKDF2 key derivation).
- [x] File System Access API support (optional, falls back to download).
- [x] Recurrence rules for future planning (monthly, annual, one-time).
- [x] Monthly charts (Chart.js – portfolio vs. debt timeline).
- [x] Export scheduling reminders (UI with configurable interval).

## v0.3 — Polish & tests (3–6 weeks)
- E2E tests for import/export & PWA install.
- [x] Accessibility audit & WCAG fixes (skip link, ARIA roles and labels throughout).
- [x] UI/UX polish and responsive layouts (dark-mode-aware inputs, improved empty states).

## v0.4 — Visual identity & usability
- [x] Light/dark mode toggle and system-preference detection.
- [x] Seven pastel themes: blue, pink, olive, beige, purple, black, white — all wired to CSS variables.
- [x] UX review: consolidated navigation, improved labels, contextual help text, reminder banner.

## v0.5 — Income & budget flexibility
- [x] Multiple named income sources (name, amount, frequency, start/end dates).
- Income projections and contribution split to savings/debt/investments.

## v0.6 — Investments & debt
- [x] Debt amortization schedule view (full month-by-month lyhennysaikataulu per debt).
- [x] Investment diversification: up to three funds with individual allocation % and expected returns, plus combined portfolio view.
- Ability to add new debt at a specific point in time (affects balance from that month onward — already supported via debt start date).

## v0.7 — Wealth and assets
- [x] Asset origin type: financed, inherited, acquired — tracked on each asset.
- [x] Vehicles: depreciation model (higher initial drop ~15 %, flattening over age) to estimate current value shown in asset table.
- Financed items: calculate estimated full-ownership date from linked payment plan; for non-vehicle items allow custom appreciation/depreciation.
- [x] Wealth summary shows total, net and liquid assets at any selected date (displayed in Overview).
