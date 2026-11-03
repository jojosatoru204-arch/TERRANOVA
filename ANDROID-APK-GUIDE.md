# TERRANOVA — Android APK build

The repository now contains a GitHub Actions workflow at `.github/workflows/build-apk.yml`.

## Add the original game ZIP

1. Upload the original HTML5 project archive to the repository root.
2. Name the uploaded archive exactly `game.zip`.
3. Commit the upload.
4. Open the **Actions** tab and select **Build TERRANOVA Android APK**.
5. If it did not start automatically, choose **Run workflow**.
6. When the run succeeds, open it and download the artifact named **TERRANOVA-Android-APK**.
7. Extract the artifact ZIP and install `app-debug.apk` on an Android device.

## Notes

- This creates a debug APK for testing, not a Play Store release build.
- The workflow expects the archive to contain an `index.html` file and its referenced assets.
- The game is copied into a Capacitor WebView. Browser-only features, remote APIs, and online multiplayer backends still need their own compatible configuration.
- GitHub Actions usage is subject to the account's included minutes and repository settings.
