# Cash Tracker — Field Ledger (PWA → APK)

This is the standalone, installable version of your cash tracker. It's a full
Progressive Web App: own icon, full-screen launch, offline support, data
saved on-device via `localStorage`.

## Step 1 — Host it somewhere (free, ~3 min)

PWABuilder needs a live HTTPS URL — it can't package local files directly.
Easiest free option, **GitHub Pages**:

1. Create a new GitHub repo (e.g. `cash-Ledger`).
2. Upload all 6 files in this folder to the repo root:
   `index.html`, `manifest.json`, `service-worker.js`, `icon-192.png`,
   `icon-512.png`, `icon-512-maskable.png`.
3. Go to **Settings → Pages**, set source to the `main` branch / root, save.
4. GitHub gives you a URL like `https://yourname.github.io/cash-Ledger/`.

(Netlify Drop — drag-and-drop the folder at app.netlify.com/drop — works too
and is even faster, no git required.)

## Step 2 — Turn it into a signed APK (~2 min)

1. Go to **pwabuilder.com**.
2. Paste your hosted URL, click **Start**.
3. PWABuilder scans it, confirms manifest + service worker are valid.
4. Click the **Android** package option → **Generate**.
5. Download the `.zip` — inside is a signed, installable `.apk`
   (plus an `.aab` if you ever want to publish to the Play Store).

## Step 3 — Install on your phone

Transfer the `.apk` to your Android device and open it. You'll need to allow
"install from unknown sources" the first time — that's Android's standard
gatekeeping for anything outside the Play Store, not a red flag on this app.

## Notes

- Your data lives in the browser/app's local storage on your device only —
  nothing is sent anywhere. If you uninstall the app, the data goes with it.
- Want it on iPhone too? No APK needed — open the hosted URL in Safari,
  tap Share → **Add to Home Screen**. Same app, same icon, no install step.
