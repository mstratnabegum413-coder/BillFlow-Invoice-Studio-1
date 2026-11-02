# Guide for AI coding tools

BillFlow is a zero-dependency static web app. Do not add a framework, bundler or CDN script.

## Architecture
- `Web App/index.html` loads scripts in order: js/invoice-calc.js, js/storage.js, js/backup.js, app.js
- `js/invoice-calc.js` pure maths (also runs in Node for tests). Exposes `BillFlowCalc`.
- `js/storage.js` the only file that touches localStorage. Exposes `BillFlowStorage`.
- `js/backup.js` JSON export/import and validation. Exposes `BillFlowBackup`.
- `app.js` UI: hash router (`#`, `#new`, `#edit-ID`, `#profile`), views, events.
- `service-worker.js` precache list: update `ASSETS` and bump `CACHE` when adding files.

## Conventions
- Escape every user value with `esc()` before inserting into HTML.
- Keep the strict CSP in index.html (no inline scripts or styles).
- Money maths only in invoice-calc.js, and add a test in tests/ for any change.

## Run locally
`npm start`, `npm test`, `npm run check`
