# Music Match Manager — GitHub Test Build

**Build:** `v2025.08.19.1550.stable6g_hotfix7`  
**Date:** 2025-08-19 15:50

This is a static, single-file web app for comparing Discogs collections A vs. B.

## How to test on GitHub Pages

1. Create or use a repo, switch to the **`gh-pages`** branch (or enable Pages in repo settings).
2. Put **`index.html`** from this folder at the repository root (or the Pages root).
3. Commit & push. GitHub Pages will serve it at your repo’s Pages URL.

## Quick start

- Open the page on desktop or mobile.
- Drag & drop or use the file pickers to load two Discogs exports (CSV) for **A** and **B**.
- Use the tabs to view **Shared** and **Only in A/B** list panes.
- Try the **Styles** section to see top styles (counts/percent toggles).

## Notes in this build

- ✅ Uses **native scrollbars** (no overlay/hide/force scripts).
- ✅ Mobile: inertial scrolling enabled via CSS only (`-webkit-overflow-scrolling: touch`).
- ✅ Version stamp lives in `<meta name="build-version">` and as `data-build-version` on `<html>`.

## Known areas to verify

- Scrollbars appear on desktop (Chrome, Edge, Firefox) and iOS/Android without duplicates.
- “Only in A/B” expand/collapse chevrons render correctly after data loads.
- Switching **Most common** ↔ **A–Z** does **not** blank the panes.
- PNG exports still render correctly (if present in this build).

## Local testing

Just open `index.html` in a modern browser. No server required. If you hit CORS issues loading local CSVs in Safari, use a simple local server:

```bash
python3 -m http.server 8080
# then visit http://localhost:8080/
```

---

© 2025 — Music Match Manager test build.
