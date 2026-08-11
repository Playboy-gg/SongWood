# SongWood 🎵

**A free, ad-free, on-device music player for Android — built around a personal listening brain, not a subscription.**

SongWood streams music from YouTube Music and JioSaavn, learns your taste entirely on your device, and turns that into a Home feed, a Daily Mix, and a continuous queue that actually gets better the more you use it — without sending your listening history anywhere.

[![License: MIT](https://img.shields.io/badge/App%20License-MIT-blue.svg)](#license)
[![Components: GPL-3.0](https://img.shields.io/badge/Streaming%20Components-GPL--3.0-orange.svg)](#license)
[![Platform](https://img.shields.io/badge/platform-Android-3DDC84.svg)](#)

---

## Table of Contents

- [Why SongWood](#why-songwood)
- [Features](#features)
- [How It Works](#how-it-works)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Roadmap](#roadmap)
- [FAQ](#faq)
- [Warnings & Disclaimers](#warnings--disclaimers)
- [Contributing](#contributing)
- [License](#license)

---

## Why SongWood

Most music apps either lock you behind a subscription or quietly ship your listening habits off to a server somewhere. SongWood was built with a simple idea: **the app should learn what you like, on your phone, and never need to ask permission to play it back to you as a better queue.**

It streams from sources that are already free (YouTube Music, JioSaavn) and spends its effort on the part that actually matters day to day — a queue and a feed that feel personal instead of generic.

## Features

### 🎧 Streaming
- **Multi-provider playback** — YouTube Music (via InnerTube) and JioSaavn, merged into one search and playback layer so a song plays from whichever source can actually serve it.
- **Cross-provider fallback** — if one source can't resolve a track, SongWood automatically looks for a playable copy on the other before giving up.
- **Gapless & crossfade playback** — built on Media3/ExoPlayer for smooth, professional-feeling transitions between tracks.
- **Offline downloads** — save songs to your device and play them with zero network dependency.

### 🧠 SongWood Brain
- An on-device recommendation engine that learns from what you actually play, skip, like, and dislike — no account, no cloud model, no data leaving your phone.
- Powers your Home feed, your Daily Mix, and the "up next" suggestions injected live into your queue while you listen.
- Shows you what it's learned — genres, artists, and moods it's picked up on — instead of being a black box.

### 🏠 A Home feed that adapts
- Personalized by your country and your chosen languages, and reshaped continuously by what you actually listen to.
- Pull-to-refresh when you want new stuff right now, not stale suggestions from this morning.

### 🎤 Lyrics
- Synced lyrics with a multi-source fallback chain, so a missing lyric source doesn't mean a silent lyrics tab.

### 🎨 Rich Now Playing experience
- High-resolution album art, a full-screen player, and a clean now-playing surface that shows what's actually loaded — not stale metadata.

### 🔔 Stay current without an app store
- In-app update checks straight from GitHub Releases, with a proper changelog you can actually read before you update — not just a version number.

### ⚙️ Built to be yours
- Country and language preferences that genuinely reshape your feed.
- A Contributors section that credits the people who work on SongWood.

## How It Works

```
 You listen, skip, like, dislike
              │
              ▼
      SongWood Brain (on-device)
   learns your taste, no cloud, no account
              │
      ┌───────┼────────┐
      ▼       ▼         ▼
  Home feed  Daily Mix  Live "up next" queue
```

1. **You play something.** Every interaction — a full listen, a skip, a like, a dislike — is a signal.
2. **The Brain learns locally.** SongWood's recommendation engine builds a picture of your taste directly on your device.
3. **Everything you see reflects it.** Your Home feed, your Daily Mix, and the songs quietly queued after your current track all come from the same learned model — not three different guessers.
4. **You stay in control.** Country and language settings shape the pool the Brain draws from; nothing is locked behind a paywall or a login.

## Tech Stack

- **Kotlin** + **Jetpack Compose** for a fully modern, declarative UI
- **Media3 / ExoPlayer** for playback, gapless transitions, and crossfade
- **Hilt** for dependency injection
- **Room** for local persistence
- **Coil** for image loading
- **InnerTube** (Kotlin) for YouTube Music access
- On-device recommendation engine ("the Brain") — no server-side ML, no telemetry

## Getting Started

> SongWood is currently under active development. Setup instructions will be finalized as the project stabilizes — check the [Releases](../../releases) page for the latest build and changelog.

1. Clone the repository
2. Open in Android Studio (or build via Gradle from the command line)
3. Build and install on a device running Android 8.0 (API 26) or newer

## Roadmap

- [ ] Deeper Brain integration across every recommendation surface (Home, Mixes, and queue all reading from one unified model)
- [ ] Improved genre/mood detection beyond keyword matching
- [ ] Scrobbling support
- [ ] Song/playlist sharing
- [ ] Expanded language and region coverage

## FAQ

**Is SongWood free?**
Yes. No subscription, no paywall, no ads.

**Does SongWood require an account or login?**
No. Everything — your history, your taste profile, your downloads — lives on your device.

**Where does the music actually come from?**
SongWood streams from existing services (YouTube Music, JioSaavn) rather than hosting any audio itself. See [Warnings & Disclaimers](#warnings--disclaimers).

**Does the Brain send my listening data anywhere?**
No. Taste learning happens entirely on-device. There's no server component reading your history.

**Why does a song sometimes fail to play?**
Streaming extraction depends on undocumented, frequently-changing behavior from third-party services. SongWood retries across providers automatically, but occasional failures are expected — see the warning below.

**Can I download songs for offline listening?**
Yes, from the song's action menu or the player's more-options sheet.

**How do updates work?**
SongWood checks GitHub Releases for new versions, shows you the changelog before you commit to anything, and can download and install the update directly — no app store required.

## Warnings & Disclaimers

⚠️ **Third-party streaming dependency.** SongWood does not host, own, or distribute any audio content. It streams from publicly accessible endpoints of third-party services (YouTube Music, JioSaavn). These services can change their internal behavior at any time without notice, which may cause playback failures until SongWood is updated to adapt.

⚠️ **No warranty.** SongWood is provided "as is," without warranty of any kind. Playback reliability, recommendation quality, and update availability are not guaranteed.

⚠️ **Personal/educational use.** This project is intended for personal and educational use. You are responsible for ensuring your use of SongWood complies with the terms of service of any third-party service it connects to, and with the laws of your jurisdiction.

⚠️ **Unofficial app installs.** If you install SongWood via a downloaded APK rather than an app store, Android will prompt you to allow installs from that source. Only do this for builds you trust (e.g. official [Releases](../../releases) from this repository).

## Contributing

Contributions, bug reports, and feature ideas are welcome. Please open an issue to discuss significant changes before submitting a pull request.

## License

SongWood uses a **dual-licensing structure**, because it's built partly from original code and partly on top of components released under copyleft terms:

- **SongWood's original application code** is licensed under the **MIT License** — see [`LICENSE`](LICENSE). You're free to use, modify, and distribute it with minimal restriction, as long as the original copyright and license notice are preserved.

- **Certain bundled streaming/extraction components** are licensed under the **GNU General Public License v3.0 (GPL-3.0)** — see [`LICENSE-GPL3`](LICENSE-GPL3). Any distribution of SongWood that includes these GPL-3.0-licensed components must comply with GPL-3.0's copyleft terms, including making corresponding source code available.

**In short:** the app itself is MIT-licensed and permissive, but because it incorporates GPL-3.0 components, redistributing a *built version* of SongWood carries GPL-3.0 obligations. If you fork or redistribute this project, review both license files before doing so.

---

<p align="center">Built for people who just want their music to sound like <em>their</em> music.</p>
