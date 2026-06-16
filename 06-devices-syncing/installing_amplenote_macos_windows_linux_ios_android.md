# Installing Amplenote

> [← Help Index](../00-index.md) · Category: [Devices & Syncing](./index.md) · [Source ↗](https://www.amplenote.com/help/installing_amplenote_macos_windows_linux_ios_android)

## Overview

This guide explains how to set up Amplenote on desktop computers, including both native app and PWA installations, enabling [offline functionality](https://www.amplenote.com/help/devices_and_syncing_work_offline).

For mobile installation instructions, see [Platform & Devices Supported](https://www.amplenote.com/help/devices_and_syncing_download_apps#How_do_I_download_mobile_apps?).

## Installing the Desktop App on Windows, macOS, or Linux

Since 2024, users with pro-level subscriptions or higher can download dedicated desktop applications. Access your [account settings](https://www.amplenote.com/account) and go to "Apps & Devices" to find platform-specific download buttons.

After downloading the executor file, run it and Amplenote will automatically install.

![Download buttons for OS-specific desktop versions](https://images.amplenote.com/8813fbca-1434-11ef-99ae-9a665e06d35f/8b5aed6f-1170-485a-9d69-2c89fd28176b.png)

## Installing the PWA on Windows, macOS, or Linux

The Progressive Web App installs through **Chrome** or **Brave** after logging in. Click the install prompt that appears in the browser interface.

After installation:
- The app becomes searchable via OS Spotlight
- A desktop icon appears (can be pinned to macOS dock)
- Browser requests permission to store data — accept this for proper functionality

![Link to install Amplenote. Note that this option becomes available after logging in to the app in Chrome or Brave.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/b54991ae-26d1-4e39-a57c-72700b62cb0b.png)

![Amplenote PWA installation dialog](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/5f64610e-9315-4c47-b660-f5eba564572d.png)

![Amplenote available via OS Spotlight search](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/e3605b8d-eefc-4ffc-af57-63f8fe7431a4.png)

![Amplenote icon pinned to the macOS dock](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/77001d71-1b8c-48ee-8b67-3e3c706985d8.png)

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

![Multiple PWA windows with calendar and note tabs open](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/73ebaa73-6fe4-43e5-aa29-5a9bfc38e0aa.png)

### Enable Tabbed Windows

1. Type `chrome://flags` in the address bar
2. Search for and enable the tabbed window settings via dropdown menus
3. Restart Chrome
4. Recreate the PWA shortcut: Navigate to amplenote.com → hamburger menu → More tools → Create shortcut
5. Select "Open as tabbed window" and confirm

![chrome://flags settings showing tabbed window options](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/ea75e1c1-cd4e-4f21-aa88-6020d7a13dc4.png)

![Chrome menu with "More tools" and "Create shortcut" options](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/266859b3-8a43-4c3d-a652-a1516b825f54.png)

![Dialog showing the "Open as tabbed window" option](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/68d047ec-9764-427d-a776-2fc1f60cfe57.png)

![Example of the final tabbed window configuration](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/a84f9d03-0413-486d-894e-5aa5635c2efb.png)

### Tab Groups

Use Chrome's tab grouping feature to visually organize calendars and note tabs with different colors and labels.

![Tab groups: a white-themed calendar group on the left and a blue group of note tabs on the right](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/0e7d8ff1-7427-4687-993b-8d5b13897cf5.png)

## Updating Amplenote

Updates download automatically, but require app restart to apply. An icon appears in the top right corner when updates are available.

![Icon that appears anytime a new update is available](https://images.amplenote.com/8813fbca-1434-11ef-99ae-9a665e06d35f/b2a54fdc-a2df-4377-b92f-b7b3f552d81a.png)

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
