# AH-AIOS Web Edition v1.4

A browser-based conversion of the supplied AH-AIOS v1.4 desktop application. The supplied dashboard screenshot is retained under `docs/` as a reference input.

## Start the website

### Option 1 — simplest

Open `index.html` in a modern desktop browser. For best compatibility with browser storage and file downloads, use Option 2.

### Option 2 — local web server (recommended)

Run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

No build step, package manager, backend, database server, or internet connection is required.

## Implemented functionality

- Responsive AH-AIOS command dashboard and animated network background.
- Working hash-based navigation for Overview, HERMES, MARA, AION, CAT, Learning Studio, Digital Product Engine, Innovation Labs, Global Network, Active Projects and Settings.
- Create, edit, search/filter, inspect and delete workspace records.
- Record fields: title, description, category/tags, status, progress and content.
- Create, edit, status-manage and delete projects.
- Global search across records and projects.
- CAT local guidance chat (deterministic help; not a remote AI model).
- Theme selection (AH-AIOS Blue, Arctic Cyan, Nebula Violet, Emerald Matrix).
- JSON workspace export and import.
- Browser-local persistence using `localStorage`.
- Responsive mobile navigation.

## Storage and capability boundaries

This is a browser-local web application. Its data is stored in the current browser profile's `localStorage`; it does not use the desktop application's SQLite database. Export JSON regularly for backup or migration. Clearing browser site data, using private browsing, or changing browser profiles may make locally stored data unavailable.

The original PySide6 application has native capabilities that a static browser application cannot directly reproduce. This web edition does **not** execute Python/PySide6, access arbitrary operating-system paths, copy files into a native library, run background agents or automation, connect to a remote AI service, or synchronize to a server. CAT is a local deterministic help interface. AION provides a workspace to capture agent/workflow information, not an execution runtime.

## Source relationship

The web edition is a new browser implementation based on the supplied AH-AIOS v1.4 source archive, including its module registry, workspace records, project management, search, chat, theme and local data concepts. The original source archive is kept offline and is not included in the deployed site.

## Verification

See `docs/VERIFICATION.md` for checks performed and known limits. SHA-256 hashes for package files are in `checksums.txt`.

## Governance state

Deliverable: AH-AIOS-WEB-001, version 1.4.0-web. Status: candidate / generated. This package has not been formally accepted or authorized for production release. Build/packaging and static checks do not substitute for Product Owner acceptance or deployment authorization.


## GitHub Pages deployment package

This ZIP is prepared for upload to the GitHub Pages deployment tool:
- `index.html` is at the ZIP root.
- `styles.css` and `app.js` are at the ZIP root and referenced with relative paths.
- Supporting documentation and the preserved original source archive are in `docs/`.
- No nested project directory needs to be selected or extracted before upload.

After deployment, open the published Pages URL and verify navigation, record/project creation, JSON export/import, and browser storage in the target browser. Deployment availability does not constitute formal product acceptance or production authorization.
