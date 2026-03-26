# Click Remote
Click Remote is a SwiftUI iOS + macOS app that turns your iPhone into a remote for Mac: media playback, volume/brightness, touchpad/mouse, scrolling, and keyboard shortcuts over local TCP with quick QR pairing.


The repository contains one app:
- `ClickRemote` (macOS menu bar server)

## For End Users

Distribution model:
- iOS app: published in the App Store https://apps.apple.com/app/click-remote/id6760541892
- macOS server: distributed as `.dmg` in GitHub Releases  https://github.com/leyfeld/Click-Remote/releases

User flow:
1. Install iOS app from the App Store.
2. Launch the iOS app and allow `Local Network` access when prompted (required to connect to your Mac).
3. Open this repository and download the latest macOS `.dmg` from Releases.
4. Install and launch the macOS app.
5. Grant permission in `System Settings -> Privacy & Security -> Accessibility`.
6. Pair devices:
   - Preferred: open menu bar icon on Mac -> `QRcode`, then scan from iOS app.
   - Alternative: add server manually via `name + ip + port`.
7. Tap a device in the list to connect and open the control screen.

Public links (replace with your real URLs):
- App Store: `https://apps.apple.com/app/click-remote/id6760541892`
- macOS DMG releases: `https://github.com/leyfeld/Click-Remote/releases`

## Features

- Control media playback: previous / play-pause / next
- Control sound: volume up / mute / volume down
- Control display brightness
- Touchpad mode: cursor move + click
- Scroll gestures
- Additional controls:
  arrow keys, `Space`, `Enter`, `Esc`, `Tab`, `Delete`, lock screen, sleep
- Quick pairing via QR code
- Manual server add by IP + port

## How It Works

- iOS app connects to macOS app over local TCP.
- Default server port: `4717`.

## Notes

- The iOS app uses Camera permission only for QR pairing.
- The iOS app uses Local Network permission to connect to your Mac.
- The macOS app must have Accessibility permission to send system key/mouse events.

## Requirements

- Xcode 15+
- iOS 17.1+ (target in project)
- macOS 13+ (target in project)
- iPhone and Mac must be on the same local network


## Tech Stack

- Swift 5, SwiftUI
- SwiftData (local persistence for devices/custom controls)
- CocoaAsyncSocket (TCP transport)
- Firebase:
  Analytics, Crashlytics, Remote Config




﻿
