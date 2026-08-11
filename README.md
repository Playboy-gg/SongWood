# SongWood 🎵

**Your Music. Zero Interruptions.**

SongWood is a beautifully designed, completely free Android music player that streams your favorite tracks directly to your device. No ads. No subscriptions. No account required. Just open the app and let the music play.

<!-- Add a screenshot here to attract users! -->

## ✨ Why You'll Love SongWood

*   **🎧 Pure Listening Experience:** Dive straight into your music. No sign-ups, no logins, and absolutely zero audio or visual ads.
*   **🌍 Massive Library:** Can't find a song? SongWood smartly fetches music from across multiple public platforms (including YouTube Music and JioSaavn) so you never miss a beat.
*   **📶 Listen Offline:** Heading somewhere without the internet? Download your favorite songs, playlists, and mixes directly to your device with a single tap.
*   **🎨 Stunning Design:** Experience a gorgeous, edge-to-edge interface that adapts to your phone's colors (Material 3) with a battery-saving deep AMOLED dark mode.
*   **🎤 Sing Along:** Enjoy synced lyrics and translations right inside the player (Beta). 
*   **🎛️ Your Sound, Your Way:** Tweak the audio exactly how you like it with our built-in Equalizer, Bass Boost, and Virtualizer (Beta).

## 🚀 How to Install

Getting started is incredibly easy:

1.  Download the latest **APK file** from our [Releases Page](https://github.com/Playboy-gg/SongWood/releases).
2.  Tap the downloaded file and select **Install** (you might need to "Allow installation from unknown sources" in your settings).
3.  **Pro Tip:** If the app asks for notification permissions, please allow it! This lets SongWood notify you and auto-update whenever a cool new feature drops. 
4.  Pick your country on the first launch to get personalized music recommendations.

---

## 🚧 What's Next? (Beta Features)

SongWood is constantly evolving! Here are a few features we are actively polishing. Expect regular updates and improvements:
*   **Smart Mixes:** Daily and topic-based mixes tailored just for you.
*   **Country-based Suggestions:** Smarter home feed recommendations based on your region.
*   **Lyrics & Translations:** Getting them perfectly synced 100% of the time.

---

## 🛠️ For Developers & Geeks

Want to see how the magic happens? SongWood is built with modern Android development practices.

**Tech Stack:**
*   Kotlin, Jetpack Compose (Material 3), Navigation
*   Hilt (Dependency Injection), Room (Local Cache), DataStore
*   Media3 / ExoPlayer for smooth playback
*   OkHttp + WorkManager for background tasks & downloads

**Build from Source:**
You'll need Android Studio (or `./gradlew`) and JDK 17. No API keys are required for default providers.

```bash
./gradlew :app:assembleDebug      # Debug APK
./gradlew :app:assembleRelease    # Signed release APK (configure signing in app/build.gradle.kts)
```
*Note: Ensure you tag releases `vX.Y.Z` and attach both the `app-release.apk` and `CHANGELOG.md` to trigger the in-app update engine properly.*

## ⚠️ Disclaimer & License

**Disclaimer:** SongWood is a personal educational project. It is not affiliated with YouTube, Google, or JioSaavn. The app utilizes reverse-engineered, publicly available unofficial APIs and free official ones (like LRCLib). Streaming availability is subject to change without notice if these endpoints are updated by their respective hosts. 

**License:** All rights reserved. This is a personal project — please do not redistribute it as your own work.
