# Steady

A personal strength + nutrition tracker. Runs entirely in the browser, stores your
data on your own phone, and installs to the home screen as an offline app.

## Files

- `index.html` — the app (and where your data is stored, via the browser)
- `sw.js` — service worker, caches the app so it opens offline
- `manifest.json` — makes it installable with a name and icon
- `icon-180.png`, `icon-192.png`, `icon-512.png` — app icons

All of these must sit in the **same folder** in your repo.

## Put it on GitHub (one time)

1. Create a new repository, e.g. `steady`.
2. Upload all the files in this zip to the repo (keep them together, root level).
3. Go to **Settings → Pages**.
4. Under **Source**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
5. Wait ~1 minute. You'll get a URL like `https://YOURNAME.github.io/steady/`.

## Install on your iPhone

1. Open that URL in **Safari** (must be Safari for install to work).
2. Tap the **Share** button → **Add to Home Screen**.
3. Launch it from the home screen — it opens full screen and works offline.

## Your data

- Logs are saved automatically on your phone as you use the app — no account, no cloud.
- **Back it up:** Plan tab → **Export backup** saves a `.json` file. Do this now and then.
- **Restore / move phones:** Plan tab → **Import backup**, pick that file.
- Clearing Safari website data, or deleting the home-screen app, erases local data —
  so keep an exported backup somewhere safe.

## Updating the app later

If you edit `index.html`, also bump the cache name in `sw.js`
(`const CACHE = 'steady-v2'` → `'steady-v3'`) so your phone pulls the new version
instead of the cached old one.
