# Room Flow Board

A single-page clinic room & queue management board. Runs entirely in the browser; optionally syncs across devices via Firebase Realtime Database.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The whole app (HTML + CSS + JS in one file). |
| `manifest.webmanifest` | PWA manifest (install to home screen). |
| `favicon.ico`, `favicon-16x16.png`, `favicon-32x32.png` | Browser tab icons. |
| `apple-touch-icon.png` | iOS home-screen icon. |
| `logo.png` | Logo shown in the app header. |
| `icons/` | All PWA icon sizes (16–1024 px). |
| `.nojekyll` | Tells GitHub Pages to serve files as-is. |

## Host on GitHub Pages

1. Create a new repository on GitHub (e.g. `room-flow-board`).
2. Upload **all** the files in this folder to the repository root
   (drag them into the "Add file → Upload files" page, then commit).
   Keep the `icons/` folder as a folder.
3. Go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Branch: `main`, folder: `/ (root)`. Save.
6. Wait ~1 minute. Your site will be live at:
   `https://<your-username>.github.io/<repo-name>/`

After any change, re-upload the file and hard-refresh the page (Cmd/Ctrl + Shift + R).

## Notes

- **Firebase sync** is already configured inside `index.html` (`FIREBASE_CONFIG`).
  Staff sign in with the login overlay; data syncs across devices.
  To run single-device only (no login), set `FIREBASE_CONFIG = null` in `index.html`.
- **Local backups**: the board auto-saves a snapshot in the browser every 10 minutes.
  Use the **🗂 Backups** button to restore one if data is ever lost.
