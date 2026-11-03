# TERRANOVA — Build Android APK

The repository contains a GitHub Actions workflow at `.github/workflows/build-apk.yml`.

## Required source archive

Upload the original HTML5 project ZIP to the repository root and name it exactly `game.zip`. It must contain `index.html` and the assets/scripts used by that page.

## Upload from Android

1. Open the repository.
2. Choose **Add file → Upload files**.
3. Select the original game ZIP from your phone.
4. Ensure its name is `game.zip` and it is at the repository root.
5. Commit the upload.

## Build and download

Uploading `game.zip` starts the build automatically. You can also open **Actions → Build TERRANOVA Android APK → Run workflow**. When every build step succeeds, open the run and download the `TERRANOVA-Android-APK` artifact. Extract it and install `app-debug.apk`.

## Build information

- App name: TERRANOVA
- Application ID: `com.kaisxstudio.terranova`
- Packaging: Capacitor 7
- Build: debug APK for testing, not a Play Store release
- CI environment: Node.js 22, Java 21, Android API 35

A successful workflow run is required before an APK exists. Packaging the HTML5 files does not itself provide an online multiplayer server; online features need a separately hosted backend and correct configuration.
