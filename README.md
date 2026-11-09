# Linkboard

[English](README.en.md)

一款跨设备粘贴板同步历史管理工具，支持局域网、蓝牙和 WebRTC 设备间传输，同步文本/图片等内容。默认本地优先，不依赖云端保存剪贴板历史；WebRTC 连接可能使用 Firebase 信令以及 STUN/TURN 服务。

## 功能特性
- 局域网 (TCP) + 蓝牙 (BLE) + WebRTC 设备间传输
- 当在同一局域网时使用 TCP，无法直连时回落到其他模式
- 跨平台支持：Android、iOS、Windows、macOS
- 文本与图片同步（图片按 PNG/JPEG 自动识别）
- 历史记录管理，支持保留天数配置与一键清理过期记录
- APP 键盘扩展：无需切出当前 App，可直接从历史粘贴
- 本地优先：不采集任何数据；支持可选、默认关闭的 WebDAV 同步

## 下载地址

- Windows 版：[下载桌面端](https://github.com/wanghongenpin/linkboard/releases/latest/download/linkboard-windows-setup.exe)
- macOS 版：[App Store](https://apps.apple.com/app/linkboard-cross-device-p2p/id6753873760)
- Android 版：[下载移动端](https://github.com/wanghongenpin/linkboard/releases/latest/download/linkboard-android.apk)
- iOS 版：[App Store](https://apps.apple.com/app/linkboard-cross-device-p2p/id6753873760)

> 如有新版本或其他平台支持，请关注项目主页或后续更新。

## 数据与隐私

WebDAV 同步是可选能力，默认关闭，且仅连接用户自行配置的 HTTPS 服务器，通过 Basic Authentication 认证。启用后可同步历史记录、收藏、固定记录及附件；服务器提供方能够读取这些数据，当前不提供端到端加密（E2EE）。

同步在应用前台运行或由用户手动触发，不保证后台执行。冲突采用确定性的最后写入者获胜（LWW）规则。为避免并发覆盖，更新已有对象时要求服务器支持强 ETag 条件写入；仅提供弱 ETag 或不提供 ETag 的服务器不能安全执行后续更新。用户主动删除会传播到其他同步端，但保留期限清理是本地行为；首个版本不会垃圾回收远端附件和删除标记（tombstones），因此它们可能继续保留在服务器上。

默认设备间传输与可选 WebDAV 同步是不同能力；WebRTC 还可能使用 Firebase 信令及 STUN/TURN 服务。详见 [PRIVACY.md](PRIVACY.md)。

## 软件截图

<img src="images/desktop.png" alt="桌面端截图" width="500"/>  <img src="images/phone.png" alt="移动端截图" width="300"/>
