# EV DriveMatch ZIP-to-APK GitHub Actions template

## One-time setup (GitHub limitation)
GitHub does not extract an uploaded ZIP into repository files, and it cannot execute a workflow that is only inside a ZIP. You must **once** extract this template ZIP and commit both `.github/workflows/build-apk.yml` and `EVDriveMatch-source.zip` to your new GitHub repository. The hidden `.github` directory is essential.

## Future builds: upload ONE ZIP only
Replace `EVDriveMatch-source.zip` in the repository using GitHub **Add file > Upload files**, commit to `main`, then open **Actions > Build APK from ZIP > Run workflow** (or wait for the push build). Download the `EVDriveMatch-debug-apk` artifact and extract `app-debug.apk`.

The source ZIP must contain a Gradle Android project with `settings.gradle(.kts)` and `app` module. Nested project directory is supported. This template builds a **debug phone APK**, not an Android Auto-compatible car-screen app. No build has been run in GitHub; first run may require troubleshooting.

If GitHub's upload UI refuses to replace an existing file, delete the old ZIP through GitHub first and upload the new one with the same name.
