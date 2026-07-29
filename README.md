# BudgetBear

BudgetBear is a client-side personal budgeting web app intended for personal use only. The application runs in the browser: no application server or account is required. Data is saved in browser `localStorage`, and you can export it to Excel, PDF, or JSON backups.

Quick highlights
- No online data storage or user account.
- Persistent local storage in the browser.
- Installable offline shell with a service worker.
- Export to Excel, PDF, and JSON backups.
- Responsive budgeting, debt, investment, and asset planning.

Getting started (local)
1. Clone the repository:
   `git clone https://github.com/kocakhakan99-beep/budgetbear.git`
2. Open `index.html` in a modern browser, or serve the repository with any static HTTP server.
3. For charts and exports, allow the CDN-hosted libraries used by `index.html`.
   The app shell and saved data remain available offline after the first load.

Application entrypoints
- `index.html` is the primary entrypoint for the refactored app shell.
- `kodin_talousstudio_v1_1.html` is retained as a legacy compatibility entrypoint.

Repository structure
- `index.html` — app shell markup
- `src/css/app.css` — shared application styles
- `src/js/app.js` — application logic and persistence
- `.github/workflows/pages.yml` — GitHub Pages deployment

Important notes about data safety
- Browser data can be cleared by the user or browser profile. Always export backups regularly.
- Exported files are not uploaded automatically; store them somewhere you control.
- The current app loads Chart.js, SheetJS, and jsPDF from CDNs, so the first load and those features require network access.

Contributing & development
- See [CONTRIBUTING.md](CONTRIBUTING.md) and [DEVELOPMENT.md](DEVELOPMENT.md).

License
- MIT — see [LICENSE](LICENSE).
