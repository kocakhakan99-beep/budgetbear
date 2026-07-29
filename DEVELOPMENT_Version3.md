# Development Guide

Goal
- Keep the application offline-only and robust: IndexedDB persistence, export/import flows, PWA installability, and client-side-only encryption option.

Prerequisites
- Node.js LTS (>=18)
- npm or yarn

Install
1. npm install

Scripts (example)
- npm run dev — start dev server (Vite / live-server)
- npm run build — build production assets
- npm run lint — run linters
- npm run test — run unit/e2e tests
- npm run preview — serve build locally for manual testing

Project structure (suggestion)
- index.html
- src/
  - js/
    - app.js
    - db.js (Dexie wrapper)
    - export.js (XLSX/JSON/export helpers)
    - import.js (parsers/validators)
    - recurrences.js (recurrence handling)
  - css/
  - assets/
- tests/

Local persistence
- Use IndexedDB via Dexie.js for the primary store.
- Keep migrations explicit (versioned Dexie schema).
- Provide a "Reset local DB" action that is protected by a confirmation modal and recommends an export first.

Export/Import
- XLSX: use SheetJS (xlsx) to create .xlsx files client-side.
- JSON: provide full structured JSON backups (for lossless import).
- Encryption: optional AES-GCM encryption of JSON backup files using Web Crypto with a passphrase.

PWA
- Add manifest.json and a Service Worker that caches the app shell and static assets.
- Do NOT cache backups or user data in the Service Worker — only the application code and static assets.

Testing
- Unit tests: transaction CRUD, import/export roundtrip, recurrence generator.
- E2E tests (Playwright): import/export flows and PWA install flow.

Security & privacy
- No network transmission by default.
- Never log user secrets to console or send backups automatically.