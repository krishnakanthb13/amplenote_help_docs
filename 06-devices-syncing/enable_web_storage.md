# How to enable web storage in the browser

> [← Help Index](../00-index.md) · Category: [Devices & Syncing](./index.md) · [Source ↗](https://www.amplenote.com/help/enable_web_storage)

## Overview

This guide covers installing Amplenote on desktop devices as either a Progressive Web App (PWA) or native application, ensuring the app functions offline. For mobile installation details, refer to the Platform & Devices Supported article.

## Installing the Desktop App on Windows, macOS, or Linux

Pro subscribers and above can download a dedicated desktop application. Access your account settings, navigate to "Apps & Devices," and download the version matching your operating system. The executable file will automatically install Amplenote upon execution.

![Download buttons for OS-specific desktop versions](https://images.amplenote.com/8813fbca-1434-11ef-99ae-9a665e06d35f/8b5aed6f-1170-485a-9d69-2c89fd28176b.png)

## Installing the PWA on Windows, macOS, or Linux

Install the Amplenote PWA using Chrome or Brave browsers by clicking the install link that appears after logging in. This action:

- Makes the app accessible via OS Search Spotlight
- Creates a dedicated icon that can be pinned to the dock (macOS)
- Prompts your browser to request data storage permission

![Link to install Amplenote. Note that this option becomes available after logging in to the app in Chrome or Brave.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/b54991ae-26d1-4e39-a57c-72700b62cb0b.png)

![Amplenote PWA installation dialog](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/5f64610e-9315-4c47-b660-f5eba564572d.png)

![Amplenote available via OS Spotlight search](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/e3605b8d-eefc-4ffc-af57-63f8fe7431a4.png)

![Amplenote icon pinned to the macOS dock](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/77001d71-1b8c-48ee-8b67-3e3c706985d8.png)

## Permitting Storage Access

Amplenote requires "web storage" or "local storage" permission to function properly. Without this access, the app can only store a few megabytes, limiting it to fewer than 100 notes without images.

### Chrome

Type `chrome://settings/content/cookies` in the address bar. Toggle the "Allow sites to save and read cookie data" setting. Note that this affects both web storage and cookies.

### Firefox

Type `about:config` in the address bar (accept any risk warnings). Locate `dom.storage.enabled` by scrolling or searching, then toggle its state via right-click menu.

For additional browser-specific assistance, contact support@amplenote.com.

## Troubleshooting the Amplenote PWA

If the PWA opens as a browser tab instead of a separate window:

1. Navigate to `chrome://apps`
2. Right-click the Amplenote icon
3. Select "Open as window"
4. Relaunch the app

![The "Open as window" context menu option](https://images.amplenote.com/c0c4fe48-79fe-11eb-847d-6a25419106f3/729a8673-e635-48eb-95c7-bcd12888ef80.png)

## Enable Multiple PWA Tabs (Beta Chrome Feature)

This feature allows multiple Amplenote instances simultaneously, such as having the calendar and multiple notes open.

![Multiple PWA windows with calendar and note tabs open](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/73ebaa73-6fe4-43e5-aa29-5a9bfc38e0aa.png)

### Enabled Tabbed Windows

1. Type `chrome://flags` in the address bar
2. Search for and enable the two settings shown in the documentation
3. Restart Chrome
4. Navigate to amplenote.com
5. Open Chrome's menu → More tools → Create shortcut
6. Select "Open as tabbed window" and create

![chrome://flags settings showing tabbed window options](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/ea75e1c1-cd4e-4f21-aa88-6020d7a13dc4.png)

![Chrome menu with "More tools" and "Create shortcut" options](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/266859b3-8a43-4c3d-a652-a1516b825f54.png)

![Dialog showing the "Open as tabbed window" option](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/68d047ec-9764-427d-a776-2fc1f60cfe57.png)

![Example of the final tabbed window configuration](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/a84f9d03-0413-486d-894e-5aa5635c2efb.png)

Use `Ctrl` + `Page Up/Down` to navigate between tabs quickly.

### Tab Groups

Use Chrome's tab group functionality to visually organize your PWA tabs by category or purpose.

![Tab groups: a white-themed calendar group on the left and a blue group of note tabs on the right](https://images.amplenote.com/d1cc0fce-469a-11ec-9b41-22ee4977f22c/0e7d8ff1-7427-4687-993b-8d5b13897cf5.png)

## Updating Amplenote

The app automatically downloads updates, but you must restart it to apply them. An icon appears in the top right corner when updates are available.

![Icon that appears anytime a new update is available](https://images.amplenote.com/8813fbca-1434-11ef-99ae-9a665e06d35f/b2a54fdc-a2df-4377-b92f-b7b3f552d81a.png)

---

## Footer Links

**Get Amplenote:**
- [Install web app](https://www.amplenote.com/help/installing_amplenote_macos_windows_linux_ios_android)
- [Download desktop app](https://www.amplenote.com/download)
- [Ample Agent Pro](https://www.amplenote.com/plugins/ample_agent_pro)
- [Google Play](https://play.google.com/store/apps/details?id=com.amplenote&hl=en)
- [App Store](https://apps.apple.com/us/app/amplenote/id1436769674)
- [Chrome Extension](https://chrome.google.com/webstore/detail/amplecap-beta-amplenote-w/jhmjlpdljfogaclolecijklcicciafaj?hl=en)
- [Firefox Extension](https://addons.mozilla.org/en-US/firefox/addon/amplecap-beta/)

**Product:**
- [Subscription pricing](https://www.amplenote.com/subscriptions/new)
- [About us](https://www.amplenote.com/about_us)
- [Product changelog](https://www.amplenote.com/product_changelog)
- [Plugin directory](https://www.amplenote.com/plugins)

**Resources:**
- [Help & learning](https://www.amplenote.com/help)
- [YouTube tutorials](https://www.youtube.com/c/Amplenote)
- [Community](https://www.amplenote.com/user_profiles)

**Social:** [Discord](https://discord.gg/nAj4wp4sJm) | [Reddit](https://reddit.com/r/amplenote) | [X](https://x.com/amplenote)
