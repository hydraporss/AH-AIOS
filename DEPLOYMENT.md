# AH-AIOS Web Edition — Deployment Notes

## Package layout
This archive is intentionally flattened for static hosting. `index.html` is in the archive root alongside `styles.css` and `app.js`.

## Deploy
1. Upload this ZIP to the After Humanity Website Deployer.
2. Choose **New repository** (or select the intended existing repository).
3. Use a repository name that is valid on GitHub; remove trailing periods or spaces.
4. Keep the repository public unless private GitHub Pages access is intentionally supported by the account plan.
5. Select **Deploy website** and wait for the deployer to report completion.
6. Open the resulting GitHub Pages URL and perform the smoke tests below.

## Smoke tests
- Overview loads without missing CSS or JavaScript.
- All workspace navigation links work.
- Create, edit, and delete a test record.
- Create and delete a test project.
- Export JSON, then import the exported JSON.
- Refresh the page and confirm test data persists in the same browser profile.
- Check the site at desktop and mobile widths.

## Important boundaries
This is a static browser-local application. Data is stored in the current browser profile's localStorage. It does not provide server-side accounts, cross-device synchronization, remote AI, or agent execution. Keep JSON exports as backups.

The package remains a candidate deliverable. A successful GitHub Pages deployment is not, by itself, Product Owner acceptance or production release authorization.
