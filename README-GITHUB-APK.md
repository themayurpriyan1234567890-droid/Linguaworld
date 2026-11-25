# LinguaWorld — GitHub APK builder

This repository packages the existing LinguaWorld website as an Android app using Capacitor. It keeps the LinguaWorld name and the website branding (`MADE BY MAYUR`).

## Build the APK with GitHub Actions

1. Create or open your existing GitHub repository: `Linguaworld`.
2. Upload **all contents** of this project ZIP to the repository root (including the hidden `.github` folder). Keep the `www` folder as-is.
3. Commit the files to the `main` branch (or `master`).
4. Open the repository's **Actions** tab.
5. Select **Build LinguaWorld APK** and press **Run workflow**. A push to `main` or `master` also starts a build.
6. When the run finishes successfully, open that workflow run and find **Artifacts** at the bottom.
7. Download `LinguaWorld-debug-apk`, extract it, and install `app-debug.apk` on your Android device. Android may ask you to allow installation from your file manager/browser.

## Notes

- This creates a **debug APK** for testing and personal installation. It is not a Play Store release-signed APK.
- The first GitHub Actions build generates the native `android/` project automatically; you do not need Android Studio on your phone.
- The app contains a local copy of the website in `www/`. Website edits must be copied into `www/` and pushed to GitHub before rebuilding.
- Existing progress/profile data is stored locally in the app's WebView. It is not automatically synced with the website browser or another device.
- Any demo sign-in or sample leaderboard in the website remains a demo; this wrapper does not add a secure account server or real online leaderboard.
- Keep `package-lock.json` after the first successful `npm install` if GitHub creates it; commit it to make later dependency installs reproducible.

## App identity

- App name: LinguaWorld
- Android application ID: `com.mayur.linguaworld`
- Web content folder: `www/`
