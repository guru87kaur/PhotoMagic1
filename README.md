# PhotoMagic AI (Android / Java)

A starter Android photo editor project. It does not use an OpenAI API key and processes edits on-device.

## Included in this first build
- Pick a photo from the phone gallery
- Adjust brightness
- Apply black-and-white and warm filters
- Rotate photo
- Save edited photo to Pictures/PhotoMagicAI

## Not included yet
This is an initial working editor, not a full generative AI editor. AI background removal, object removal, AI enhancement/upscaling, and generative background replacement still need model integration and testing.

## Build an APK
1. Install Android Studio (current stable version) on a Windows, Mac, or Linux computer.
2. Open this `PhotoMagicAI` folder in Android Studio.
3. Allow Gradle sync and install Android SDK Platform 35 if prompted.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. Android Studio will show the APK location, normally `app/build/outputs/apk/debug/app-debug.apk`.

Requirements: Android Studio with Android SDK Platform 35 and JDK 17. The project uses Android Gradle Plugin 8.6.1.

## Build in the cloud (no Android Studio needed on your phone)
This project includes `.github/workflows/build-apk.yml`. To build an APK using GitHub Actions:
1. Create a GitHub account (if you do not have one) and create a new repository.
2. Upload the contents of this project folder to that repository.
3. Open the repository's **Actions** tab and select **Build PhotoMagic AI APK**.
4. Choose **Run workflow** and wait for the run to finish successfully.
5. Open the completed run and download the `PhotoMagicAI-debug-apk` artifact. Extract it to get `app-debug.apk`.
6. Transfer `app-debug.apk` to your Android phone, tap it, and allow installation from that source if Android asks.

This produces a debug APK for testing. It is not a Play Store release-signed APK. The workflow has not been run from this environment, so its output must be verified in GitHub Actions before installation.
