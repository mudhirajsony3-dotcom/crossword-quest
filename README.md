# Crossword Quest — Free 50-level game

A self-contained, responsive crossword web app. It has 50 themed levels, clue lists, a generated crossword grid, keyboard entry, reveal-letter and reveal-word hints, level unlocking, scoring, local progress saves, and installable PWA files.

## Run locally on a computer

1. Unzip the project.
2. Open a terminal in the `crossword-free` folder.
3. Run `python3 -m http.server 8000` (or `python -m http.server 8000`).
4. Open `http://localhost:8000` in a browser.

Opening `index.html` directly works for basic play, but service-worker/offline installation needs a local server or HTTPS hosting.

## Put it online for free

1. Create a GitHub account if you don't have one.
2. Create a public repository, e.g. `crossword-quest`.
3. Upload `index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`, and this README.
4. In repository Settings → Pages, select deploy from the `main` branch and `/ (root)`.
5. Wait for the GitHub Pages URL, then open it on your phone.

Other free static hosting providers can work too. Use HTTPS for PWA installation.

## Install on Android

1. Open the hosted HTTPS URL in Chrome on Android.
2. Tap Chrome's ⋮ menu → **Install app** or **Add to Home screen** (wording can vary).
3. Confirm. It will appear on your home screen and launch in a standalone window.

This is an installable web app (PWA), not an APK from the Play Store. It costs nothing to test and use. Publishing a native Android app to Google Play is a separate process and may require a developer registration fee.

## Game notes

- The 50 levels and clue/answer content are bundled in `index.html` in the `LEVELS` array.
- Progress and points are stored in the browser's local storage on the current device/browser.
- Crossword placement is generated in the browser. Because automatic placement can vary, review each generated grid and clue set before public release. For a production release, replace the generator with hand-checked grid layouts and add broader device/browser testing.
