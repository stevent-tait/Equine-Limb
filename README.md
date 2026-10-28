# Equine Limb Atlas

An interactive, colour-coded anatomy atlas of the horse's left fore- and hindlimb in lateral view. Bones, muscles, tendons and ligaments, arteries, veins and nerves are drawn as separate layers and labelled with their Latin (Nomina Anatomica Veterinaria) names. Tapping a name opens its description, function, connections within the limb and to the rest of the body, and a close-up diagram.

It is a static Progressive Web App: no build step, no server code. It installs to the home screen on iOS and Android and works offline after the first visit.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: drawings, anatomy text and interface |
| `manifest.webmanifest` | App name, colours and icons for installation |
| `sw.js` | Service worker that caches the app for offline use |
| `icons/` | Home-screen icons (Android, iOS and maskable) |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Publish on GitHub Pages

1. Create a public repository (for example `equine-limb-atlas`) and push these files to the `main` branch.
2. In the repository go to **Settings → Pages**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, and save.
3. After a minute the app is live at `https://<your-username>.github.io/equine-limb-atlas/`.

## Install on a phone

- **iPhone / iPad (Safari):** open the link, tap **Share**, then **Add to Home Screen**.
- **Android (Chrome):** open the link, tap the **⋮** menu, then **Install app** (or **Add to Home screen**).

## Updating

Edit `index.html`, then increase `VERSION` in `sw.js` (for example `v2` → `v3`) so installed copies fetch the new version. Users see a short "Updated" notice and get the new version next time they open the app.

## Notes

The drawings are simplified for study. Structures that lie on the medial side of the limb, or deep to others, are dashed so they remain visible in a single lateral view.
