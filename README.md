# AgriPro Timeline

A self-contained, bilingual (English / 中文) durian phenology & input-planning PWA.
Single file, offline-capable, no build step, no external dependencies.

## Files
- `index.html` — the entire app (HTML + CSS + JS + embedded icon).
- `sw.js` — service worker; caches the app shell so it works offline.
- `.nojekyll` — tells GitHub Pages to serve files as-is.

## Host on GitHub Pages
1. Upload `index.html`, `sw.js`, and `.nojekyll` to the repository root
   (https://github.com/stanleywoosweeleong/agriprotimeline).
2. Repo **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*,
   Branch = `main`, folder = `/ (root)`. Save.
3. The app will be live at:
   **https://stanleywoosweeleong.github.io/agriprotimeline/**

## Install on a phone
- **Android (Chrome):** open the link → menu → *Add to Home screen* / *Install app*.
- **iPhone (Safari):** open the link → Share → *Add to Home Screen*.
  If you redeploy and the icon looks old, remove the app and re-add it — iOS caches the icon.

## Updating the app
Replace `index.html` with the new version. Installed devices refresh from the network
on their next online launch (navigations are network-first). To *force* every device to
refresh, also bump the cache name in `sw.js` (e.g. `agripro-timeline-v1` → `-v2`).
