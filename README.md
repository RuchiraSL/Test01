# Nifti Tech Invoicing — Android App

This repository is configured for a one-click APK build with GitHub Actions.

## One-click APK build

1. Upload the **contents of this folder** to a GitHub repository.
2. Open the repository on GitHub.
3. Go to **Actions**.
4. Select **Build Android APK**.
5. Click **Run workflow**.
6. Wait for the green check mark.
7. Open the completed workflow run and download the **NiftiInvoicing-APK** artifact.
8. Extract the downloaded artifact to get `NiftiInvoicing-debug.apk`.

The workflow installs Android SDK 34 and Build Tools 34.0.0 automatically, uses Java 17 and Gradle 8.7, and builds an installable debug APK.

## Automatic builds

A push to the `main` or `master` branch also starts the APK build automatically.

## Local Android Studio build

Open this `NiftiInvoicing` folder in Android Studio and let Gradle sync. The project uses:

- Android Gradle Plugin 8.5.2
- Gradle 8.7
- Compile SDK 34
- Minimum SDK 26
- Java 17

## Important: release signing

The GitHub workflow intentionally produces a **debug APK**, which is suitable for testing and direct installation. A Play Store release requires a release keystore and signing configuration; do not commit a private keystore or passwords to the repository.
