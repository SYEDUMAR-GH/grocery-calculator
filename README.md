# Grocery Weight & Price Calculator (PWA)

A installable, offline-capable Progressive Web App.

## Files
- `index.html` — the app
- `manifest.json` — PWA metadata (name, icons, theme color)
- `sw.js` — service worker (caches the app so it works offline)
- `icons/icon-192.png`, `icons/icon-512.png` — app icons

## Deploy on GitHub Pages

1. Create a new GitHub repository (e.g. `grocery-calculator`).
2. Upload all the files in this folder to the repo root, keeping the `icons/` folder structure intact.
3. On GitHub: go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Set **Branch** to `main` (or `master`) and folder to `/ (root)`, then **Save**.
6. Wait a minute, then your app will be live at:
   `https://<your-username>.github.io/<repo-name>/`

### Using git from a terminal instead
```bash
git init
git add .
git commit -m "Grocery calculator PWA"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```
Then enable Pages as in steps 3–5 above.

## Install it on a phone
Open the GitHub Pages link in Chrome (Android) or Safari (iOS):
- **Android/Chrome**: tap the menu → "Install app" or "Add to Home screen".
- **iOS/Safari**: tap Share → "Add to Home Screen".

It will then open full-screen, with its own icon, and keep working without internet once it has loaded once.

## Notes
- If you rename the repo or move files into a subfolder, double-check the paths in `manifest.json` and `index.html` (`manifest.json`, `icons/...`) still resolve correctly relative to `index.html`.
- To push an update later, bump `CACHE_NAME` in `sw.js` (e.g. `grocery-calc-v2`) so installed users get the new version instead of a stale cached copy.
- 
