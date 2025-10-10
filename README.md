# UniClip

一款跨设备剪贴板同步工具，支持局域网与蓝牙双通道，同步文本/图片等内容。项目基于 Flutter 构建，开箱即用、无云端依赖，数据仅在你的设备之间本地传输与保存。

## 功能特性
- 局域网 (TCP) + 蓝牙 (BLE) 双通道同步
  - 当在同一局域网时使用 TCP，无法直连时回落到低功耗蓝牙
- 跨平台支持：Android、iOS、Windows、macOS、Linux
- 文本与图片同步（图片按 PNG/JPEG 自动识别）
- 历史记录管理，支持保留天数配置与一键清理过期记录
- APP 键盘扩展：无需切出当前 App，可直接从历史粘贴
- 完全本地化：不依赖任何云服务，不采集任何数据

## 下载地址

- [Windows 版下载](https://example.com/uni_clip/windows)
- [macOS 版下载](https://example.com/uni_clip/macos)
- [Linux 版下载](https://example.com/uni_clip/linux)
- [Android 版下载](https://example.com/uni_clip/android)
- [iOS 版下载](https://example.com/uni_clip/ios)

> 如有新版本或其他平台支持，请关注项目主页或后续更新。

## 数据与隐私
UniClip 致力于最小权限与本地化处理：
- 不依赖云端服务器，所有同步数据仅在你的设备之间直连传输
- 数据仅保存在本地设备上（包括历史记录、配置等）
- 我们不采集任何个人信息，不做行为跟踪，不做遥测
- 你可随时在应用内清理历史记录
- 蓝牙权限与定位权限仅用于蓝牙扫描/连接/广播，不会在后台收集任何与剪贴板无关的信息

若你对隐私有更多要求，可在系统层面限制网络访问或蓝牙权限，UniClip 仍可在受限能力范围内工作（例如仅在局域网或仅在蓝牙下工作）。
