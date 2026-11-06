# LANShare 局域网快传

零流量、跨设备极速互传的 Android 应用。无需移动数据、无需登录账号，同一 Wi-Fi 下即可在手机与电脑之间高速传输文件。

## 功能特性

- **零流量传输**：所有数据走局域网，不消耗移动数据
- **跨设备互传**：Android / Windows / macOS 浏览器均可参与
- **自动发现**：基于局域网广播，自动识别同网段设备
- **多文件并发**：支持批量选择、断点续传
- **无广告无后台**：轻量、纯净、即用即走

## 下载安装

- 最新 APK：[点此下载](https://aka.doubaocdn.com/s/SVY6stz4V7)（v1.4.0，约 4.5 MB）
- 或在本仓库 Releases 中获取历史版本

> 安装时如提示"未知来源"，请在系统设置中允许浏览器安装应用。

## 源码

源码打包在 `lanshare-src.zip` 中，包含完整 Android 工程：

- Kotlin 源码（`app/src/main/java/com/lanshare/app/`）
- 资源文件（布局、图标、字符串）
- Gradle 构建脚本

## 本地构建

需要 JDK 11 与 Android SDK 33：

```bash
./gradlew assembleRelease
```

产物在 `app/build/outputs/apk/release/`。

## 技术栈

- Kotlin + 标准 Android SDK
- 基于 WifiP2p / UDP 广播做设备发现
- 自建 TCP 协议做文件传输
- 前台服务维持长连接

## 许可

本仓库源码仅供学习交流使用。APK 仅供个人安装使用，未经许可不得用于商业用途。
