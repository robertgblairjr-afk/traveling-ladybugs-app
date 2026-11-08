# The Traveling Ladybugs

A children's detective and learning game (ages 3 to 6) from Lisa Blair's picture book. No ads, no accounts, nothing collected.

## What is in this repo

| Path | What it is |
|---|---|
| `site/` | The playable web game (static files, no build step). This is what Cloudflare Pages hosts. |
| `TravelingLadybugs.apk` | The Android and Amazon Fire tablet app (same game, packaged). |

**Download the tablet app:** [TravelingLadybugs.apk](https://github.com/robertgblairjr-afk/traveling-ladybugs-app/raw/main/TravelingLadybugs.apk)

## Host the web game on Cloudflare Pages

1. Cloudflare dashboard > **Workers & Pages** > **Create** > **Pages** > **Connect to Git**.
2. Pick this repo (`traveling-ladybugs-app`) and branch `main`.
3. Build settings: **Framework preset: None**. **Build command:** leave empty. **Build output directory:** `site`.
4. Save and Deploy. Every push to `main` redeploys automatically.
5. Optional: Custom domains > add your domain once the company has one.

## Install on an Amazon Fire tablet
1. Open this page in the Silk browser and tap the download link above.
2. When it finishes, tap the file (or open **Files** > **Downloads** and tap it).
3. If asked, allow installs from Silk (or Files): Settings > Security & Privacy > Apps from Unknown Sources.
4. Tap **Install**, then **Open**.

To update, download and install the newer file the same way. Saved progress is kept.

From version 23.19 on, the app checks `version.json` here when it starts and shows grown-ups a "New version ready" button on the start screen when a newer APK is up. Bump `code` (the APK versionCode) and `name` in `version.json` with every new APK.

The Traveling Ladybugs, characters and game are owned by Traveling Ladybugs, LLC. Developed by Gloss Mountain Games, LLC.
