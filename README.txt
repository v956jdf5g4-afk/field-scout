FIELD SCOUT V5 — OFFLINE IPAD TEST BUILD

This is a progressive web app (PWA). It must be hosted over HTTPS for service-worker offline caching and iPad Home Screen installation. Opening index.html directly from a ZIP or local file is NOT sufficient to test offline installation.

1. Upload the entire contents of this folder to an HTTPS static web host (e.g., Netlify Drop). Keep index.html, sw.js, manifest.webmanifest, and both PNG icons together.
2. On iPad Safari, open the HTTPS URL while online. Tap Share > Add to Home Screen > Add.
3. Launch from the Home Screen while online once; wait for the page to load.
4. Turn on Airplane Mode, close the app, relaunch from its Home Screen icon, add a test note, save, force-close, and relaunch. Check the note and plan survived.
5. Turn Wi-Fi back on. Use Back up all data to save a JSON backup into Files/iCloud Drive. Test restoring it in a separate test browser before relying on it.

IMPORTANT: Local IndexedDB storage is device/browser-specific and can still be removed by the operating system, storage pressure, user actions, or private browsing. This is NOT a production backup strategy. No cloud sync, server database, login, encryption, or multi-device sharing yet. Do not use as sole storage for real scouting records.

The app attempts to migrate prior V4 notes and plan from localStorage, but only when V5 runs on the SAME web origin as the old version. A local file or preview on a different origin cannot be automatically migrated. Export existing test data separately.

This is a self-contained static app with no third-party runtime dependencies.
