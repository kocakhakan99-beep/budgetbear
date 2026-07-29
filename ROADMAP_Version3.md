# Roadmap (offline-first)

Priority: get a stable offline experience and robust export/import before adding advanced features.

v0.1 — Offline core (1–2 weeks)
- UI for basic transactions, categories, budgets.
- IndexedDB persistence via Dexie.
- Export to XLSX and JSON.
- Import JSON and XLSX with validation.
- PWA shell (manifest + Service Worker).

v0.2 — Reliability & UX (2–4 weeks)
- Client-side encryption for JSON backups.
- File System Access API support (optional).
- Recurrence rules for future planning.
- Monthly charts (Chart.js or Chartist).
- Export scheduling reminders (UI only).

v0.3 — Polish & tests (3–6 weeks)
- E2E tests for import/export & PWA install.
- Accessibility audit & WCAG fixes.
- UI/UX polish and responsive layouts.