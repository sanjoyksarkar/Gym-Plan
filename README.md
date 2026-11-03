# Momentum Gym — Installable Offline Workout App (PWA)

This is an installable Progressive Web App (PWA) version of your Office Gym Master HTML tracker.
It is not an Android APK. No Play Store publication or app server is required.

## Included
- Five-day Sunday–Thursday workout plan (3:00–4:00 PM)
- Cardio and strength exercise logging, notes, set weights and repetitions
- Exercise diagrams and technique guides; stopwatch/rest timer
- Weight progress chart, daily step log and workout history
- JSON backup/restore and CSV export
- Standalone app icon, offline cache, Android/iOS browser installation support
- Private local storage: there is no account, tracking script or remote database

## Install on Android (recommended: GitHub Pages)
1. Unzip this ZIP. Keep index.html, sw.js, manifest.webmanifest and icons/ together.
2. Put these files in a new GitHub repository; for a public GitHub Pages site, avoid putting personal logs in the repo.
3. In repository Settings -> Pages, deploy the main branch from the root folder.
4. Open the resulting HTTPS GitHub Pages URL in Chrome on your Android phone.
5. Tap the in-app **Install** control, or Chrome's menu -> **Install app** / **Add to Home screen**.
6. Launch from the new Momentum Gym app icon. Visit online once before switching to offline use.

Note: web installability requires HTTPS or localhost. Opening index.html from Downloads works as a normal local browser page but cannot install it as a PWA.

## iPhone
Use Safari (or supported browser) -> Share -> Add to Home Screen after HTTPS hosting.

## Existing tracker records
The old standalone office_gym_master.html and the installed PWA do not share storage. In the old file, choose Settings -> Backup JSON, then in this app choose Settings -> Restore JSON. Do this *before* adding new records, because restore replaces current data.

## Run locally for testing (computer)
From the extracted directory:
    python3 -m http.server 8080
Then open http://localhost:8080 on your computer. Some browsers will allow PWA install from localhost.
For phone access, local LAN HTTP (e.g. http://192.168.x.x:8080) isn't a secure context, so the install/offline worker may be unavailable; use HTTPS hosting.

## Privacy and limitations
- Data stays in the browser's localStorage on the same device. It is not automatically synchronized or backed up. Export JSON regularly.
- Clearing browser/app storage can permanently erase logs.
- Exercise illustrations are original simplified diagrams; third-party exercise-library links require internet.
- No automated push reminders and no native Android APK in this package.
