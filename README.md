# CAOCAP

CAOCAP is an early-stage project for a programmable AI copilot with computer-use skills for macOS. This repository contains separate native macOS and iOS app projects.

## Current status

Both apps currently launch a SwiftUI “Hello, world!” screen. AI integration, programmable skills, and computer-use functionality are not implemented yet.

The apps use Swift and SwiftUI, with no external package dependencies configured.

## Run locally

You need a Mac with Xcode and SDKs that support the configured deployment targets:

| App | Deployment target |
| --- | --- |
| macOS | macOS 26.5 |
| iOS | iOS 26.5 |

Both projects were created with Xcode 26.6 and use Swift 5 language mode.

From the repository root, open the project you want to run:

```sh
# macOS app
open Apps/macOS/caocap/caocap.xcodeproj

# iOS app
open Apps/iOS/caocap/caocap.xcodeproj
```

In Xcode, select the `caocap` scheme and choose **My Mac** for macOS or a compatible simulator for iOS, then press **⌘R**. The app should display a globe icon and “Hello, world!”. To run on a physical iOS device, select your development team under **Signing & Capabilities** and choose the connected device.

## Repository layout

| Path | Contents |
| --- | --- |
| `Apps/macOS/caocap/` | macOS Xcode project, SwiftUI source, and asset catalog |
| `Apps/iOS/caocap/` | iOS Xcode project, SwiftUI source, and asset catalog |
| `Assets/brand/appicons/` | Brand app icon sets |
| `Assets/brand/cdl-v2/` | Character artwork, visual references, and asset manifest |

Each app has its own `caocapApp.swift` entry point and `ContentView.swift` initial screen. Make UI changes in the corresponding platform directory; the projects do not currently share a code module.

## Brand assets

See the [CDL v2 asset manifest](Assets/brand/cdl-v2/MANIFEST.md) for Cocaptain and CoStar artwork, intended uses, and review notes. The manifest includes references to app integration that is not present in these starter projects; use the Swift source and each app’s `Assets.xcassets` catalog to check what is currently wired up.

## Validation

There are no automated test targets configured yet. After changing an app, build and run its Xcode project and check the affected screen.
