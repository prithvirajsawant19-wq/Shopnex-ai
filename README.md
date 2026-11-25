# ShopSmart AI — Android Studio project

This wraps the existing ShopSmart AI HTML/CSS/JavaScript prototype in a simple Android WebView app so it can be built as an APK and installed on an Android tablet.

## Important
This ZIP is the **Android app source project**, not a precompiled APK. Building an APK requires Android Studio and the Android SDK. This environment has prepared the project files but has not compiled or tested an APK on a physical device.

## Build an APK
1. On a Windows, Mac or Linux computer, install the latest stable Android Studio: https://developer.android.com/studio
2. Extract `ShopSmart-AI-Android.zip`.
3. In Android Studio choose **Open** and select the extracted `ShopSmart-AI-Android` folder.
4. Allow Android Studio to sync Gradle and install Android SDK Platform 35 if prompted.
5. If prompted to use a newer compatible Gradle/Android Gradle Plugin, accept Android Studio's recommended upgrade.
6. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
7. When the build finishes, click **locate** in the notification. The APK is normally at:
   `app/build/outputs/apk/debug/app-debug.apk`
8. Transfer `app-debug.apk` to your Android tablet, open it, and allow installation from that file manager if Android asks.
9. Launch **ShopSmart AI** from the tablet app drawer.

## What this app does
- Opens the ShopSmart AI prototype as an Android app.
- Uses the tablet's screen size and responsive layout.
- Enables JavaScript and browser local storage for the prototype.
- Keeps the sample inventory and recorded sales in the app's local WebView storage.

## Current limitations
- This is a local demo; it has no cloud sync, user login or live AI API connection.
- The “AI Advisor” uses predefined JavaScript business rules, not a live AI model.
- Data is stored on that tablet inside the app. Clearing app storage or uninstalling the app can erase it.
- The app currently does not need internet permission because all screens and logic are bundled locally.
- Before using this for real business records, add backup, authentication, cloud database, security and proper accounting/tax handling.

## Project layout
- `app/src/main/assets/` — index.html, style.css, script.js
- `app/src/main/java/com/shopsmart/ai/MainActivity.kt` — Android WebView host
- `app/src/main/AndroidManifest.xml` — app configuration
- `app/build.gradle` — Android build configuration
