# Installing OfflineWord

## Easiest: let GitHub build the installers
1. Push this folder to a GitHub repo (branch `main`).
2. Open the **Actions** tab → *Build installers* (runs automatically on push, or press *Run workflow*).
3. When finished, download the artifacts at the bottom of the run:
   - **OfflineWord-Windows** → `OfflineWord Setup 1.0.0.exe` (installer) and a portable `.exe`
   - **OfflineWord-Android-APK** → `app-debug.apk`

## Windows 11
Run the Setup `.exe` (Windows SmartScreen may warn because the app is unsigned: *More info → Run anyway*).
Or build locally: install Node.js 20, then `npm install` and `npm run dist:win` → files appear in `dist/`.
To test without installing: `npm install` then `npm start`.

## Huawei MatePad
**Option A – APK (HarmonyOS 2/3/4 and EMUI, which run Android apps):** copy `app-debug.apk` to the tablet, open it in Files and allow *Install unknown apps*. Documents save to the *Documents* folder and open the share sheet.
**Option B – PWA (any tablet, no APK):** host the `app/` folder with GitHub Pages (Settings → Pages), open the URL once in Huawei Browser / Chrome / Edge and choose *Add to Home screen*. It then works offline.
Note: HarmonyOS NEXT does not run APKs; use Option B there.

## Local Android build (optional)
Needs Android Studio + JDK 17: `npm install`, `npx cap add android`, `npx cap sync android`, `npx cap open android`, then *Build → Build APK*.
