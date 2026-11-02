# BillFlow - Invoice Studio

A static, offline-first invoice app for freelancers and small businesses. Create invoices, track Paid / Outstanding / Overdue, print or save PDFs, and keep a JSON backup. No account, backend, external API, CDN, or third-party dependency is required.

## Features
- Dashboard totals for Paid, Outstanding, and Overdue invoices
- Search and filter invoices
- Invoice editor with live preview, line items, tax, discount, notes, and currency selection
- Create, edit, duplicate, and delete invoices
- Business profile and invoice-number prefix
- Print / Save as PDF
- JSON backup export and import
- Sample invoices for trying the app
- Responsive layout, light/dark theme, and offline-ready PWA

## Deploy with GitHub Pages
1. Upload the **contents** of this project to the repository root (not the ZIP file and not inside an extra folder).
2. Keep the `.github/workflows/pages.yml` file and its folder path.
3. In GitHub, open **Settings → Pages** and choose **GitHub Actions** as the build and deployment source.
4. Open **Actions** and wait for **Deploy BillFlow to GitHub Pages** to finish successfully.
5. Your URL will be `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

All app asset paths are relative, so the site works from a GitHub Pages repository subpath.

## Run and test locally
- `npm start` then open `http://localhost:8080`
- `npm test` runs invoice calculation tests
- `npm run check` checks JavaScript syntax

## Data and privacy
Invoices and profile settings are stored in this browser's localStorage under `billflow.v1`. Data does not sync between devices. Clearing browser data can erase invoices; use **Profile → Export backup** regularly. There is no server-side storage.

## Project layout
- `index.html`, `styles.css`, `app.js`
- `js/storage.js`, `js/invoice-calc.js`, `js/backup.js`
- `service-worker.js`, `manifest.webmanifest`, `icon.svg`
- `.github/workflows/pages.yml`
- `tests/invoice-calc.test.js`, `docs/data-format.md`

## Licence
See `LICENSE-NOTE.md` for the supplied Vibe96 licence note.
