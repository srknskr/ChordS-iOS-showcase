# ChordS for iOS

A music and rhythm companion for browsing, practicing, and playing chord- and loop-oriented content.

## About

ChordS brings musical content, loop playback, tempo control, playlists, repeat practice, and an equalizer-oriented listening experience into an iOS application. The private project is organized around shared SwiftUI views, view models, models, helpers, and services, with localized resources and a shared audio-engine layer.

This public repository is a documentation-only showcase. Production source code, audio assets, Firebase configuration, signing material, store credentials, and private media remain private.

## Screenshots

<p align="center">
  <img src="./IMG_0662.png" width="220" alt="Create Loop screen before adding chords" />
  <img src="./IMG_0663.png" width="220" alt="Create Loop screen with chord timeline" />
  <img src="./IMG_0978.png" width="220" alt="Equalizer screen" />
</p>

## Highlights

- Music and rhythm content browsing
- Loop playback with BPM and repeat controls
- Custom loops and playlist organization
- Saved tempo and practice-oriented playback state
- Equalizer-oriented listening controls
- Localized UI and App Store metadata
- Background playback and Live Activity support
- Firebase analytics, messaging, and in-app messaging
- Google Mobile Ads integration
- Xcode workspace/project and Fastlane metadata workflow

## Architecture

~~~mermaid
flowchart TD
    VIEW[SwiftUI views] --> VM[View models]
    VM --> MODEL[Music, loop, and playlist models]
    VM --> SERVICE[Shared application services]
    SERVICE --> ENGINE[Shared audio engine]
    ENGINE --> PLAYBACK[Playback, BPM, and repeat]
    VM --> EQ[Equalizer-oriented controls]
    APP[App state and Live Activity] --> SERVICE
    SERVICE --> FIREBASE[Firebase services]
    RELEASE[Fastlane metadata] --> ASC[App Store Connect]
~~~

The application separates SwiftUI presentation from view models, content models, and shared services. Playback-related state is coordinated by the service layer and passed to the shared audio engine, while app integrations and delivery automation stay outside the core content flow.

## Technology

| Area | Implementation |
| --- | --- |
| UI | SwiftUI |
| App structure | Shared views, view models, models, helpers, and services |
| Audio | Shared audio engine for music and loop playback |
| Playback features | BPM, repeat, background playback, Live Activity support |
| Platform services | Firebase Analytics, Firebase Messaging, Firebase In-App Messaging |
| Monetization | Google Mobile Ads SDK |
| Delivery | Xcode workspace/project and Fastlane |
| Targets | iOS 15+ target; macOS target also exists in the private workspace |
| Localization | Multiple localized resource bundles |

## Repository scope

Only showcase documentation and product screenshots are public here. No production Swift source, Firebase configuration, signing certificates, provisioning profiles, API keys, App Store Connect credentials, or private production media are included.
