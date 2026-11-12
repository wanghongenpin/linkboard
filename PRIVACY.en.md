# Linkboard Data & Privacy Policy

[中文文档](PRIVACY.md)

Last updated: November 9, 2026

Linkboard follows local-first and least-privilege principles. This policy explains how Linkboard handles clipboard content, device information, and network connection data.

## Local data

- Clipboard history, favorites, pinned items, attachments, and settings are stored on your device by default. We do not rely on developer-operated cloud storage for your clipboard history.
- History is cleaned according to the retention period you configure in the app. You can also delete individual records or clear history manually.
- We do not include advertising, behavioral analytics, or advertising telemetry SDKs, and we do not sell your data.

## Permissions

- Bluetooth permissions are used for scanning, connecting, and advertising so that data can be transferred between your devices.
- Some Android versions or devices require location permission for Bluetooth scanning. This permission is used only for system Bluetooth functionality, not to track your location.
- Camera permission is used to scan QR codes for device pairing.
- Saving images and selecting files only processes the relevant content when you initiate those actions.

If optional permissions are declined, the app can still operate with reduced capabilities, such as LAN-only or Bluetooth-only mode.

## Remote pairing, online presence, and WebRTC

When “Remote sync” is enabled (currently the default), or when you actively use remote pairing or WebRTC connections, the app uses third-party network services:

- **Firebase Realtime Database**: used for device pairing, online presence, and WebRTC signaling. Processed data may include raw or hashed device identifiers, pairing codes, online timestamps, encrypted pairing information, and connection information such as SDP/ICE. Firebase may also process network IP addresses and standard service logs.
- **STUN/TURN services**: used to discover network addresses and establish or relay WebRTC connections. Their providers may process IP addresses, network metadata, and connection times. When a TURN relay is used, encrypted traffic from the WebRTC data channel passes through that relay.
- Firebase signaling is not used to store clipboard history. Device-to-device transfers and signaling are separate processes; WebRTC content travels through the data channel rather than being written to Firebase as clipboard history.

This data is used only to provide pairing, online presence, and device connectivity, not for advertising or behavioral tracking. Third-party services also process data under their own privacy policies. You can disable Remote sync in the app settings to stop subsequent remote presence updates and related connection features.

## Retention and deletion

- Local records are cleaned according to your retention settings and can also be deleted manually. Uninstalling the app may remove app data, depending on the operating system and backup settings.
- WebRTC signaling messages are deleted on a best-effort basis after processing. Expired pairing or signaling data may be ignored or removed. However, online presence records and residual data left by offline states or failed requests are not currently guaranteed to expire or be deleted immediately.
- Disabling Remote sync stops subsequent updates but does not automatically delete all previously uploaded records. To request deletion of residual remote data associated with your device, contact us using the email below and provide the information needed to locate the records.

## Optional WebDAV sync

WebDAV sync is disabled by default and is used only after you explicitly configure and enable it:

- It connects only to your configured HTTPS WebDAV server using Basic Authentication. The app does not select a default synchronization provider or switch you to another provider.
- It can synchronize history, favorites, pinned items, and their attachments.
- Data is not end-to-end encrypted (E2EE). HTTPS protects data in transit, but the server provider can read synchronized data and attachments stored on the server.
- Sync runs while the app is in the foreground or when manually triggered and is not guaranteed to run in the background.
- Conflicts are resolved using deterministic last-writer-wins (LWW) rules.
- Explicit user deletions propagate to other sync peers. Retention-based cleanup is local to each device and is not a unified remote retention policy.
- The current version does not garbage-collect remote attachments or deletion tombstones. They may remain on the server after the corresponding records disappear from the app and must be managed or deleted through your server.

Leaving WebDAV sync disabled prevents synchronization data from being sent to a WebDAV server.

## Policy updates and contact

When this policy changes, the date above will be updated and the revised policy will be published on this page.

Developer: wanghongenpin

Contact: [wanghongenpin@gmail.com](mailto:wanghongenpin@gmail.com)
