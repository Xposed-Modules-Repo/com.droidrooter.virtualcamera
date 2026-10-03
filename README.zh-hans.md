# DRVCAM

[English](README.md) | [Español](README.es.md) | [العربية](README.ar.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Italiano](README.it.md) | [日本語](README.ja.md) | **简体中文**

**适用于已 root 的兼容 Android 设备的虚拟摄像头。** 选择一张照片或一段视频，把它作为你所选应用的摄像头画面，支持实时播放和取景控制。

[![最新版本](https://img.shields.io/github/v/release/Xposed-Modules-Repo/com.droidrooter.virtualcamera?label=最新版本)](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases/latest)
[![平台](https://img.shields.io/badge/平台-Android-3DDC84)](#运行要求)
[![需要-root](https://img.shields.io/badge/需要-root-critical)](#运行要求)
[![许可](https://img.shields.io/badge/许可-proprietary-lightgrey)](#许可)

> **Alpha 版本。** DRVCAM 仍在积极开发中，具体表现可能因设备而异。

本仓库是 DRVCAM 的**模块列表条目**，不包含源代码。产品页面、价格和完整文档：**[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**。

## 目录

- [截图](#截图)
- [功能说明](#功能说明)
- [运行要求](#运行要求)
- [下载](#下载)
- [安装](#安装)
- [免费版与付费套餐](#免费版与付费套餐)
- [隐私须知](#隐私须知)
- [常见问题](#常见问题)
- [免责声明](#免责声明)
- [许可](#许可)
- [支持](#支持)
- [更新日志](#更新日志)

## 截图

| 主页 | 悬浮控制器 |
|---|---|
| ![DRVCAM 主界面：实时画面预览、目标应用选择、媒体来源和快捷控制](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-home.webp) | ![悬浮控制器叠加在摄像头应用上](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-controller.webp) |

| 媒体编辑器 | 预设 |
|---|---|
| ![媒体编辑器：播放、循环、缩放和旋转控制](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-editor.webp) | ![媒体库的预设标签页](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-presets.webp) |

## 功能说明

- 在设备、摄像头 API 和应用支持的范围内，将你导入的照片或视频用作所选应用的摄像头来源。
- 让你选择目标应用，并调整播放、旋转、镜像、缩放和取景。可以保存并切换一个 Main 来源和两个预设。
- 让你在虚拟画面和真实物理摄像头之间切换已配置的目标。部分应用需要重新打开摄像头才能显示变化，DRVCAM 会在需要时提示你。
- 提供可选的悬浮控制器，始终显示在你正在使用的应用上方（需要悬浮窗权限）。
- 不改变真实麦克风 — DRVCAM 不会替换或处理音频。

## 运行要求

- 已 root 的 Android 设备（Magisk 或 KernelSU），Android 9 及以上版本。摄像头替换需要 root；没有 root 时应用可以打开，但无法使用替换功能。
- 支持 libxposed API 102 的 Xposed 系列框架 — DRVCAM 使用 [Vector](https://github.com/JingMatrix/Vector)（LSPosed 的后继项目）进行测试，这是一个基于 Zygisk 的 LSPosed 系列框架。不支持 API 102 的框架无法加载该模块。
- 为所选媒体和应用提供足够的解码与图形处理能力。

## 下载

此列表提供 **Android 12 及以上版本的手机构建版本**（arm64）。其他构建版本——Android 9 至 11 及模拟器镜像——位于 **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**，并配有选择工具为你推荐合适的版本。

此处每个版本都会在发行说明中提供 SHA-256 — 安装前请先校验下载文件。

## 安装

1. 下载并安装与你的 Android 版本和设备类型相符的 APK（见上表）。
2. 打开你的框架管理器并启用 DRVCAM，如有提示请重启设备。
3. 打开 DRVCAM，并在提示时授予 root 权限。DRVCAM 会在自身应用内管理所选应用的授权范围 — 你无需在框架管理器中手动添加任何内容。
4. 登录，或选择 **免费试用**（参见[免费版与付费套餐](#免费版与付费套餐)）。
5. 将照片或视频导入媒体库，选中它，选择目标应用，然后点击 **Enable**。请自行打开目标应用的摄像头。
6. 在目标应用内查看结果。DRVCAM 自身的预览有助于挑选素材，但单凭预览并不能证明目标应用已经收到画面。

**Disable** 会再次移除 DRVCAM 对该目标的授权范围。

## 免费版与付费套餐

DRVCAM 需要一个 DRVCAM 账号和网络连接来完成登录、设备注册和续期。登录后，应用可以在一定期限内离线继续使用。

- **免费试用**（无需付费）：图片源，一个目标应用。
- **付费套餐**：视频源、多个目标应用、悬浮控制器以及 Camera Source 切换。

当前套餐、设备数量上限及价格：**[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/#pricing)**。

## 隐私须知

- 你的媒体文件在摄像头工作流程中始终保留在你的设备上 — 账号服务不需要你的媒体内容或摄像头画面来完成登录。
- 账号服务会处理账号、设备和订阅数据，以保证登录和授权正常工作。诊断信息仅在你主动请求时才会发送。
- 目标应用仍可能保存、分析或传输其摄像头所显示的内容；这取决于该应用自身的隐私政策。
- 完整政策：[droidrooter.com/privacy](https://www.droidrooter.com/privacy)。

## 常见问题

**需要 root 吗？**
需要。摄像头替换通过系统级 Hook 实现，需要 root 以及兼容的 Xposed 系列框架。

**能在我的设备上使用吗？**
产品页面只列出了已验证的组合。设备、固件和摄像头应用的差异很大，无法提前保证兼容性。

**可以不登录使用吗？**
可以，使用**免费试用**（图片源，一个目标应用）。视频和其他功能需要付费套餐。

**忘记密码怎么办？**
目前账号找回需要人工处理，请使用下方[支持](#支持)中的联系方式。

**源代码在哪里？**
本仓库不发布源代码。本仓库是模块列表条目，仅分发经过签名的发行版二进制文件。

## 免责声明

DRVCAM 是 Alpha 版软件，按“现状”提供，不附带任何形式的保证。对设备进行 root 以及安装无系统签名的框架，均由你自行承担风险，可能影响设备保修或稳定性。

你需要自行对所使用的媒体内容、搭配 DRVCAM 使用的应用程序，以及遵守适用于你的法律和条款负责。开发者不对本软件的任何非法、未经授权或其他不当使用承担责任。

## 许可

DRVCAM 为闭源专有软件。本软件不授予任何复制、修改、逆向工程或再分发的许可。下载和安装行为受产品网站上公布的[使用条款](https://www.droidrooter.com/terms)约束。

## 支持

- Telegram：[@DroidRooter](https://t.me/DroidRooter)
- 网站联系表单：[droidrooter.com/contact](https://www.droidrooter.com/contact)

## 更新日志

具体变更请查看每个 [发行版](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases)的说明。
