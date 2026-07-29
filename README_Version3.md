# BudgetBear

BudgetBear is an offline-first personal budgeting web app intended for personal use only. The application runs entirely in the browser: no data is stored online by default. The app helps you track transactions, plan budgets, and project future recurring expenses. Data is saved locally (IndexedDB) and you can export to Excel (.xlsx) or JSON to "save" data externally.

Quick highlights
- Entirely offline-first (no online data storage).
- Persistent local storage via IndexedDB.
- Export to Excel (.xlsx) and JSON backups.
- Optional client-side encryption for backups.
- Installable as a PWA for better offline reliability.

Getting started (local)
1. Install Node.js (LTS)
2. Clone:
   git clone https://github.com/kocakhakan99-beep/budgetbear.git
3. Install:
   npm install
4. Start dev server:
   npm run dev
5. Open http://localhost:3000

Important notes about data safety
- Browser data can be cleared by the user or by the browser (cache, site data, profile deletion). Always export backups regularly.
- Use the Export feature to create XLSX or encrypted JSON backups you control.
- If you want automatic persistent file saves, enable/make use of the File System Access API (only available in some browsers).

Contributing & development
- See CONTRIBUTING.md and DEVELOPMENT.md.

License
- MIT — see LICENSE.