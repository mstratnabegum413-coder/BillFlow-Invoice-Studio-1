# BillFlow setup

## GitHub Pages
1. Put the contents of this folder at the repository root. Do not upload the ZIP itself and do not nest the files under `Web App/` or another folder.
2. In repository **Settings → Pages**, set the source to **GitHub Actions**.
3. The included `.github/workflows/pages.yml` deploys on every push to `main` and can also be run manually from **Actions**.
4. Wait for the workflow to finish, then open `https://USERNAME.github.io/REPOSITORY/`.

## Render (optional)
If using a static host instead, publish the repository root (`.`) with no build command. GitHub Pages is the primary deployment route for this package.

## First use
Open **Profile** to enter business details and default currency/tax, then select **New invoice**. On an empty dashboard, use **Load sample data** to try example invoices.

## Offline check
First open the site while online and allow the service worker to install. Then use the browser's offline mode or disconnect briefly and reload. Service workers require HTTPS or localhost.
