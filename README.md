# The Traveling Ladybugs

A children's detective and learning game (ages 3 to 6) from Lisa Blair's picture book. No ads, no accounts, nothing collected.

## What is in this repo

| Path | What it is |
|---|---|
| `site/` | The playable web game (static files, no build step). This is what Cloudflare Pages hosts. |
| `TravelingLadybugs.apk` | The Android and Amazon Fire tablet app (same game, packaged). |

**Download the tablet app:** [TravelingLadybugs.apk](https://pub-117426033f4140e1a99daa9b98081d81.r2.dev/TravelingLadybugs.apk) (hosted on Cloudflare R2; GitHub only holds files under 100 MB, so from app 89 on the newest APK lives there).

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

From version 23.19 on, the app checks `version.json` here when it starts and shows grown-ups a "New version ready" button on the start screen when a newer APK is up. Bump `code` (the APK versionCode) and `name` in `version.json` with every new APK. `version.json` may also carry a `url` (https) for the APK; the "New version ready" button uses it, otherwise the R2 link above. Tablets still on app 88 or older have the GitHub copy of the APK baked in as their link, so the copy in this repo stays at app 89 (the last one that fits) and tablets on 88 get 89 from it once; after that, updates come from R2.

The Traveling Ladybugs, characters and game are owned by Traveling Ladybugs, LLC. Developed by Gloss Mountain Games, LLC.
