# Linkboard

A cross-device clipboard sync and history manager supporting LAN, Bluetooth, and WebRTC device-to-device transfer. It is local-first by default and does not require cloud storage for clipboard history; WebRTC connections may use Firebase signaling and STUN/TURN services.

[中文文档](README.md)

## Features
- Device-to-device transfer over LAN (TCP), Bluetooth (BLE), and WebRTC
- Uses TCP on the same LAN; falls back to other modes when direct connection is not possible
- Cross-platform: Android, iOS, Windows, macOS
- Sync text and images (auto-detect PNG/JPEG)
- History management with configurable retention days and one-tap cleanup
- App keyboard extension: paste from history without leaving the current app
- Local-first with no data collection; optional WebDAV sync is available and disabled by default

## Downloads

- Windows: [Download Desktop](https://github.com/wanghongenpin/linkboard/releases/latest/download/linkboard-windows-setup.exe)
- macOS: [App Store](https://apps.apple.com/app/linkboard-cross-device-p2p/id6753873760)
- Android: [Download Mobile](https://github.com/wanghongenpin/linkboard/releases/latest/download/linkboard-android.apk)
- iOS: [App Store](https://apps.apple.com/app/linkboard-cross-device-p2p/id6753873760)

> For new releases or additional platform support, follow the repository.

## Data & Privacy

WebDAV sync is optional and disabled by default. It connects only to your configured HTTPS server, whose provider can read the synced data; end-to-end encryption is not provided. Sync runs in the foreground or when triggered manually. See [PRIVACY.en.md](PRIVACY.en.md).

## Screenshots

<img src="images/desktop.png" alt="Desktop screenshot" width="500"/>  <img src="images/phone.png" alt="Mobile screenshot" width="300"/>
