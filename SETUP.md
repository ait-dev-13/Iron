# Iron Log — Install as an Android App

This folder turns Iron Log into a **PWA (Progressive Web App)** — installs to your
home screen with its own icon, opens full-screen with no browser bar, and works
offline. No Play Store, no coding, no APK.

## Important: it needs to be hosted online first

Android's "install as app" feature only works over **HTTPS**. Opening
`index.html` straight from your phone's file storage will *not* give you the
install prompt. You need to put these files somewhere with a real URL first.
The easiest free option is **GitHub Pages**:

### Steps (about 5 minutes, one-time)

1. Go to [github.com](https://github.com) and log in (or create a free account).
2. Click **+** → **New repository**. Name it something like `iron-log`. Set it
   to **Public**. Click **Create repository**.
3. On the new repo page, click **Add file → Upload files**.
4. Drag in all the files from this folder:
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
   - the `icons` folder (with all 4 PNGs inside)
5. Scroll down, click **Commit changes**.
6. Go to the repo's **Settings** tab → **Pages** (left sidebar).
7. Under "Build and deployment," set **Source** to **Deploy from a branch**,
   branch **main**, folder **/ (root)**. Click **Save**.
8. Wait about a minute, then refresh — GitHub will show you a live URL like:
   `https://yourusername.github.io/iron-log/`

### Install on your Android phone

1. Open that URL in **Chrome** on your phone.
2. Tap the **⋮** menu → **Add to Home screen** (or you may see an automatic
   "Install app" banner — tap it).
3. Confirm. Iron Log now appears on your home screen with its own icon, and
   opens full-screen like a native app.

Your workout data is stored locally on your phone (not on GitHub), so it stays
private and works even with no signal. Use the **Download Backup** button in
the app periodically to save a copy to Google Drive, just in case.

## Updating the app later

If you ever want changes made to Iron Log, just re-upload the updated
`index.html` (and any changed files) to the same GitHub repo, overwriting the
old ones. Your phone will pick up the update automatically next time you open
the app with a connection.

## Alternative: skip hosting entirely

If you don't want to deal with GitHub Pages, you can still just open
`index.html` directly in Chrome on your phone (via a file manager app or by
emailing it to yourself). It'll work fine as a normal web page and save data
locally — you just won't get the home-screen icon / full-screen / offline
install experience, since that requires HTTPS hosting.
