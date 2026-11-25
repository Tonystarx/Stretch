# Stretch Timer

A stretch routine timer built for iPhone. Build routines from an exercise bank, reorder them by dragging, and run them with a timer that handles left and right sides automatically.

## Features

- Several named routines, built from a bank of 34 starter stretches, each with a line figure. You can add your own.
- Comes with two starter routines: Daily Full Body, and Bikram + CrossFit Mobility.
- Each stretch is either one-sided or left/right. Left/right stretches run the full time on each side, with a 5-second switch countdown between sides.
- Times of 1, 2 or 3 minutes per stretch (default 1).
- Between stretches, choose Timed (a 5-second "Starts in" countdown, adjustable) or Manual (the next stretch waits until you tap play or forward).
- Next/Back step through each side.
- Changes to a routine's stretches are held until you choose Save, Save as new routine, or Discard. Rename a routine with the pencil next to its name.
- Sound cues for the last 3 seconds, the side switch and each start.
- Works offline after the first visit, and installs to the Home Screen with its own icon.
- Data is saved on the device. Export/Import in Settings handles backups.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app |
| `manifest.webmanifest` | App name, colors and icons for Home Screen install |
| `sw.js` | Service worker that lets the app open offline |
| `icons/` | Home Screen and browser icons |

## Publish on GitHub Pages

1. Create a new repository on GitHub, for example `stretch-timer`. On a free GitHub account it must be **Public** to use Pages.
2. On the repository page, click **Add file > Upload files**. Drag in `index.html`, `manifest.webmanifest`, `sw.js`, `README.md` and the whole `icons` folder. Then click **Commit changes**.
3. Go to **Settings > Pages**. Under "Build and deployment", set **Source** to **Deploy from a branch**. Set **Branch** to `main` and the folder to `/ (root)`, then click **Save**.
4. Wait a minute or two, then refresh the Pages settings screen. Your site address appears at the top, in the form `https://<your-username>.github.io/stretch-timer/`.

## Install on iPhone

1. Open the site address in **Safari**.
2. Tap the **...** button next to the address bar, then **Share**, then **Add to Home Screen**.
3. Leave **Open as Web App** on and tap **Add**.

Open the app once while you're online so it can save itself for offline use.

## Backups

Your routines are stored on the phone, inside the installed app. To keep a copy or move them to another device:

- **Settings > Export backup** saves a `.json` file. On iPhone, pick **Save to Files** or AirDrop it.
- **Settings > Import backup** restores from that file. This replaces what's currently on the device.

On iPhone, the Home Screen app may keep its data separate from the same site opened in Safari. Use the Home Screen app as your main copy.

## Updating the app

1. Replace `index.html` (and any other changed files) in the repository.
2. In `sw.js`, change `stretch-timer-v1` to `stretch-timer-v2` (then `v3`, and so on). This makes phones pick up the new version promptly.
3. Open the app twice. The first launch downloads the update in the background, and the second launch shows it.

Your saved routines are kept across updates.
