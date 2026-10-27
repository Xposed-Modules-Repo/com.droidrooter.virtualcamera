<div align="center">

<img src="assets/logo.png" width="96" alt="DRVCAM logo">

# DRVCAM

**A virtual camera for compatible rooted Android devices.** Choose a photo or video and present it as the camera feed of the apps you select, with live playback and framing controls.

**English** | [Español](README.es.md) | [العربية](README.ar.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Italiano](README.it.md) | [日本語](README.ja.md) | [简体中文](README.zh-hans.md)

[![Latest release](https://img.shields.io/github/v/release/Xposed-Modules-Repo/com.droidrooter.virtualcamera?label=latest%20release)](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases/latest)
[![Platform](https://img.shields.io/badge/platform-Android-3DDC84)](#requirements)
[![Root required](https://img.shields.io/badge/root-required-critical)](#requirements)
[![License](https://img.shields.io/badge/license-proprietary-lightgrey)](#license)

**[⬇ Download](#download)** &nbsp;·&nbsp; **[📦 Install](#install)** &nbsp;·&nbsp; **[💬 Support](#support)** &nbsp;·&nbsp; **[🌐 droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**

</div>

> [!IMPORTANT]
> **Beta release.** DRVCAM is under active development and behaviour can vary by device. This repository is the **module listing** for DRVCAM. It does not contain source code. Product page, pricing and full documentation: **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**.

## Table of contents

- [Screenshots](#screenshots)
- [What it does](#what-it-does)
- [Requirements](#requirements)
- [Download](#download)
- [Install](#install)
- [Free plan and paid plans](#free-plan-and-paid-plans)
- [Privacy basics](#privacy-basics)
- [FAQ](#faq)
- [Disclaimer](#disclaimer)
- [License](#license)
- [Support](#support)
- [Changelog](#changelog)

## Screenshots

<div align="center">
<table>
<tr>
<td align="center"><img src="screenshots/screen-home.webp" width="200"><br><sub>Home</sub></td>
<td align="center"><img src="screenshots/screen-controller.webp" width="200"><br><sub>Floating Controller</sub></td>
<td align="center"><img src="screenshots/screen-editor.webp" width="200"><br><sub>Media editor</sub></td>
<td align="center"><img src="screenshots/screen-presets.webp" width="200"><br><sub>Presets</sub></td>
</tr>
</table>
</div>

## What it does

- Uses a photo or video that you import as the camera source of an app you select, where the device, camera API and app support it.
- Lets you choose the target apps and adjust playback, rotation, mirror, zoom and framing. A Main source and four presets can be saved and switched.
- Lets you switch a configured target between the virtual feed and the real physical camera. Some apps need their camera reopened before a change appears; DRVCAM tells you when that is the case.
- Offers an optional floating controller that stays above the app you are using (needs the overlay permission).
- Leaves the real microphone unchanged — DRVCAM does not replace or process audio.

## Requirements

- A rooted Android device (Magisk or KernelSU), Android 9 and newer. Camera replacement needs root; without it the app opens but replacement is unavailable.
- An Xposed-family framework that supports libxposed API 102 — DRVCAM is tested with [Vector](https://github.com/JingMatrix/Vector) (the successor of LSPosed). A framework without API 102 support will not load the module.
- Enough decoder and graphics capacity for the media and app you choose.

## Download

This listing carries the **phone build for Android 9 and newer** (arm64). The emulator image is on **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**, with a picker that recommends the right one for your device.

Every release here includes its SHA-256 in the release notes — verify your download before installing.

## Install

1. Download and install the APK that matches your Android version and device type (above).
2. Open your framework manager and enable DRVCAM, then reboot if it asks you to.
3. Open DRVCAM and grant root when prompted. DRVCAM manages the scope of the apps you select from inside its own app — you do not need to add anything by hand in the framework manager.
4. Sign in, or choose **Try Free** (see [Free plan and paid plans](#free-plan-and-paid-plans)).
5. Import a photo or video into Library, select it, choose a target app, then **Enable**. Open the target app's camera yourself.
6. Check the result inside the target app. DRVCAM's own preview helps you pick media; it does not by itself prove the target app received the feed.

**Disable** removes DRVCAM's scope from the target again.

## Free plan and paid plans

DRVCAM needs a DRVCAM account and an internet connection for sign-in, device registration and renewal. After signing in, the app can keep working offline for a limited period.

- **Try Free** (no cost): image sources, one target app.
- **Paid plans**: video sources, several target apps, the floating controller and the Camera Source switch.

Current plans, device limits and prices: **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/#pricing)**.

## Privacy basics

- Your media stays on your device for the camera workflow — the account service does not need your media or camera frames to sign you in.
- The account service processes account, device and subscription data so that sign-in and licensing work. Diagnostics are sent only when you request them.
- A target app can still save, analyse or transmit what its camera shows; that app's own privacy practices apply.
- Full policy: [droidrooter.com/privacy](https://www.droidrooter.com/privacy).

## FAQ

<details>
<summary><strong>Does this need root?</strong></summary>

Yes. Camera replacement is delivered through a system-level hook that requires root and a compatible Xposed-family framework.
</details>

<details>
<summary><strong>Will it work on my device?</strong></summary>

Only verified combinations are listed on the product page. Device, firmware and camera app vary too much to promise support in advance.
</details>

<details>
<summary><strong>Can I use it without signing in?</strong></summary>

Yes, with **Try Free** (image sources, one target app). Video and the other features need a paid plan.
</details>

<details>
<summary><strong>Does it replace my microphone too?</strong></summary>

No. DRVCAM only replaces what the camera sees. The real microphone is left untouched, whichever plan you're on.
</details>

<details>
<summary><strong>Can I use a live network stream as my camera source?</strong></summary>

Yes, on a paid plan. Import an RTSP/RTMP stream the same way you'd import a photo or video.
</details>

<details>
<summary><strong>How many camera setups can I save?</strong></summary>

A Main setup plus four presets. Presets need a paid plan; Main is available on the free plan too.
</details>

<details>
<summary><strong>What does Remote Diagnosis do?</strong></summary>

It lets support connect to your device to help diagnose an issue. It's off by default — you turn it on yourself in Settings only when you want help.
</details>

<details>
<summary><strong>I lost my password — what do I do?</strong></summary>

Account recovery is manual for now; use the [Support](#support) links below.
</details>

<details>
<summary><strong>Where is the source code?</strong></summary>

Not published here. This repository is a module listing with signed release binaries only.
</details>


## Disclaimer

DRVCAM is beta software, provided "as is" without warranty of any kind. Rooting a device and installing a systemless framework are actions you take at your own risk and may affect your device's warranty or stability.

You are solely responsible for the media you use, for the applications you use DRVCAM with, and for complying with the laws and the terms that apply to you. The developer is not responsible for any illegal, unauthorized or otherwise improper use of this software.

## License

DRVCAM is proprietary, closed-source software. No licence to copy, modify, reverse-engineer or redistribute the application is granted. Downloading and installing it is governed by the [Terms of Use](https://www.droidrooter.com/terms) published on the product site.

## Support

- WhatsApp: [Chat on WhatsApp](https://wa.me/message/RPNSAAK4EPUSC1)
- Telegram: [@DroidRooter](https://t.me/DroidRooter)
- Website contact form: [droidrooter.com/contact](https://www.droidrooter.com/contact)

## Changelog

See the notes on each [release](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases) for what changed.
