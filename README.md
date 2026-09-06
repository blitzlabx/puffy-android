# Puffy AI — Android (Kotlin)

[![Android Build](https://github.com/blitzlabx/puffy-android/actions/workflows/android-build.yml/badge.svg)](https://github.com/blitzlabx/puffy-android/actions/workflows/android-build.yml)

**Puffy AI by Blitz** · native **Kotlin** Android app  
App ID: `com.blitzlabx.puffy`

## What this is
A pure Kotlin Android app (`MainActivity.kt`) that hosts Puffy AI in a configured WebView pointing at:

`https://puffy-ai.onrender.com`

You get the full chat, memory, Markdown, images, PDF/ZIP experience without rewriting the whole product in Compose.

## Why Kotlin (not Capacitor JS shell)
- Real Android project: Gradle + Kotlin + AndroidManifest  
- Installable **APK** via GitHub Actions  
- System back button, status bar, network security config in native code  

## GitHub Actions (recommended)
1. Push **this folder** (or the whole `puffy-android` project) as a GitHub repo root.
2. Actions → **Android Build** → **Run workflow** → choose **debug**.
3. Download artifact **puffy-ai-debug-apk** → install `app-debug.apk` on your phone.

## Local build (Android Studio)
1. Open this folder in Android Studio.
2. Let it sync Gradle (downloads wrapper if needed).
3. Run → Run 'app' or **Build → Build APK(s)**.

```bash
# CLI (needs Android SDK + wrapper jar)
./gradlew assembleDebug
# APK: app/build/outputs/apk/debug/app-debug.apk
```

## Change backend URL
Edit `MainActivity.kt`:

```kotlin
const val PUFFY_URL = "https://puffy-ai.onrender.com"
```

## Creator
Blitz · blitzlabx · https://t.me/blitzmax
