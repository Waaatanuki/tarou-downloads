# Tarou 下载

本仓库提供 Tarou 扩展、Windows、macOS 和 Android 客户端的安装包与更新信息。

- [下载最新版本](https://github.com/Waaatanuki/tarou-downloads/releases/latest)
- [使用文档](https://waaatanuki.github.io/tarou-docs/)

## 选择安装包

在最新 Release 的 **Assets** 中选择对应平台的文件，`<version>` 为该 Release 的版本号。

| 平台 | 安装包 |
| --- | --- |
| Chrome / Chromium 扩展 | `Tarou-Extension-<version>.zip` |
| Windows x64 | `Tarou-<version>-win-x64-setup.exe` |
| macOS Apple Silicon | `Tarou-<version>-mac-arm64.dmg` |
| Android | `Tarou-Android-<version>.apk` |

`.blockmap` 和 `latest.yml` 供 Windows 自动更新使用，无需手动下载。本仓库目前不提供 Intel Mac 或 iOS 安装包。

## 安装与更新

### 浏览器扩展

1. 下载扩展 ZIP 并解压，保留其中的 `Chrome-Extension-Tarou` 文件夹。
2. 打开浏览器的扩展管理页，例如 Chrome 的 `chrome://extensions/`，开启「开发者模式」。
3. 点击「加载已解压的扩展程序」，选择 `Chrome-Extension-Tarou` 文件夹。

有新版本时，菜单头像上方会显示蓝色下载按钮，点击下载新版 ZIP。更新时用新版文件替换原目录中的内容，保持加载路径不变，再在扩展管理页点击「重新加载」；必要时刷新游戏页面。不要通过删除已安装扩展的方式更新，以免清空本地数据。

### Windows

下载并运行 `win-x64-setup.exe`，按安装向导完成安装。

有新版本时，菜单头像上方会显示蓝色下载按钮。第一次点击下载更新，下载完成后按钮变为「重启安装」，再次点击才会保存数据、退出并安装。应用不会自动下载，也不会在普通退出时安装更新。

支持跨版本升级，例如 `4.0.0` 可以直接更新到 `4.0.2`，无需逐个安装中间版本。自动更新失败时，可以完全退出 Tarou 后运行最新版安装包覆盖安装，无需先卸载，保留本地配置和记录。

### macOS

仅支持 Apple Silicon（M 系列芯片）。下载并打开 `mac-arm64.dmg`，将 `Tarou.app` 拖入「应用程序 / Applications」。

当前应用未经过 Apple 公证。如果系统提示 Apple 无法验证 Tarou，确认安装包来自本仓库的 Release 后，进入「系统设置 → 隐私与安全性」，找到 Tarou 并选择「仍要打开」。

有新版本时，菜单头像上方的蓝色下载按钮会通过浏览器下载 DMG。更新时先完全退出 Tarou，再将新版 `Tarou.app` 拖入「应用程序」并选择替换，无需先卸载，保留本地配置和记录。

### Android

下载 APK 后打开安装；首次安装时，按系统提示允许当前浏览器或文件管理器安装应用。

有新版本时，打开应用内菜单，点击「菜单」标题右侧的蓝色下载按钮，通过系统浏览器下载新版 APK。下载完成后手动打开 APK 覆盖安装，无需先卸载，保留本地配置和记录。

## 版本与更新说明

扩展、Windows、macOS 和 Android 使用统一版本号，Release tag 为 `major.minor.patch`，例如 `4.0.2`。各端检测的更新日志位于仓库根目录的 [changelog.json](https://github.com/Waaatanuki/tarou-downloads/blob/main/changelog.json)，Windows 自动更新元数据位于根目录的 `latest.yml`。
