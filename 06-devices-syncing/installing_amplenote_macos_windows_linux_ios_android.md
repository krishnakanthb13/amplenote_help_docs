# Installing Amplenote

> [← Help Index](../00-index.md) · Category: [Devices & Syncing](./index.md) · [Source ↗](https://www.amplenote.com/help/installing_amplenote_macos_windows_linux_ios_android)

## Overview

This guide explains how to set up Amplenote on desktop computers, including both native app and PWA installations, enabling [offline functionality](https://www.amplenote.com/help/devices_and_syncing_work_offline).

For mobile installation instructions, see [Platform & Devices Supported](https://www.amplenote.com/help/devices_and_syncing_download_apps#How_do_I_download_mobile_apps?).

## Installing the Desktop App on Windows, macOS, or Linux

Since 2024, users with pro-level subscriptions or higher can download dedicated desktop applications. Access your [account settings](https://www.amplenote.com/account) and go to "Apps & Devices" to find platform-specific download buttons.

After downloading the executor file, run it and Amplenote will automatically install.

## Installing the PWA on Windows, macOS, or Linux

The Progressive Web App installs through **Chrome** or **Brave** after logging in. Click the install prompt that appears in the browser interface.

After installation:
- The app becomes searchable via OS Spotlight
- A desktop icon appears (can be pinned to macOS dock)
- Browser requests permission to store data — accept this for proper functionality

## Permitting Storage Access

Amplenote requires web storage permission to function properly. Without it, the app can only store a few megabytes (under 100 notes, typically no images).

### Chrome

Type `chrome://settings/content/cookies` in the address bar and toggle "Allow sites to save and read cookie data."

### Firefox

Enter `about:config` in the address bar. Search for `dom.storage.enabled` and toggle its state via right-click menu.

## Troubleshooting PWA Window Issues

If the app opens as a browser tab instead of a separate window:

1. Navigate to `chrome://apps`
2. Right-click the Amplenote icon
3. Select "[Open as window](https://images.amplenote.com/c0c4fe48-79fe-11eb-847d-6a25419106f3/729a8673-e635-48eb-95c7-bcd12888ef80.png)"
4. Relaunch the app

## Enable Multiple PWA Tabs (Beta Chrome Feature)

This feature allows running multiple Amplenote windows simultaneously (calendar plus notes, for example). Use `Ctrl + Page Up/Down` to switch between tabs.

### Enable Tabbed Windows

1. Type `chrome://flags` in the address bar
2. Search for and enable the tabbed window settings via dropdown menus
3. Restart Chrome
4. Recreate the PWA shortcut: Navigate to amplenote.com → hamburger menu → More tools → Create shortcut
5. Select "Open as tabbed window" and confirm

### Tab Groups

Use Chrome's tab grouping feature to visually organize calendars and note tabs with different colors and labels.

## Updating Amplenote

Updates download automatically, but require app restart to apply. An icon appears in the top right corner when updates are available.

---

## Get Amplenote

**Installation Options:**
- [Install web app](https://www.amplenote.com/help/installing_amplenote_macos_windows_linux_ios_android)
- [Download desktop app](https://www.amplenote.com/download)
- [Ample Agent Pro](https://www.amplenote.com/plugins/ample_agent_pro)

**Mobile Apps:**
- [Google Play](https://play.google.com/store/apps/details?id=com.amplenote&hl=en)
- [App Store](https://apps.apple.com/us/app/amplenote/id1436769674)

**Browser Extensions:**
- [Chrome Amplecap](https://chrome.google.com/webstore/detail/amplecap-beta-amplenote-w/jhmjlpdljfogaclolecijklcicciafaj?hl=en)
- [Firefox Amplecap](https://addons.mozilla.org/en-US/firefox/addon/amplecap-beta/)
