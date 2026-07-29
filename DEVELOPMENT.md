# Development Guide

## Prerequisites

No build toolchain is currently required. Use a modern browser and, optionally, a
static HTTP server for local development.

## Run locally

Open `index.html` directly, or serve the repository root:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>. The application currently loads Chart.js,
SheetJS, and jsPDF from CDNs, so network access is required for the initial load
and those integrations.

## Project structure

- `index.html` — application shell and UI markup
- `src/css/app.css` — application styles
- `src/js/app.js` — state, calculations, rendering, and import/export
- `kodin_talousstudio_v1_1.html` — legacy compatibility entrypoint
- `.github/workflows/pages.yml` — GitHub Pages deployment

## Data and backups

Application state is stored under the `kt-state` key in browser `localStorage`.
Use the Data page to export JSON backups regularly. Excel and PDF exports are
reporting formats; JSON is the lossless restore format.

Never commit exported user data or credentials. Test imports with disposable
data and verify that reset operations are intentional.

## Validation

There is currently no package manifest, automated test suite, or lint
configuration. Before submitting a change, open the app in a browser and
manually exercise the affected workflow, including export/import when relevant.