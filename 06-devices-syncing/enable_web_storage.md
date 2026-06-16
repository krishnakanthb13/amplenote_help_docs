# How to enable web storage in the browser

> [← Help Index](../00-index.md) · Category: [Devices & Syncing](./index.md) · [Source ↗](https://www.amplenote.com/help/enable_web_storage)

## Overview

This guide covers installing Amplenote on desktop devices as either a Progressive Web App (PWA) or native application, ensuring the app functions offline. For mobile installation details, refer to the Platform & Devices Supported article.

## Installing the Desktop App on Windows, macOS, or Linux

Pro subscribers and above can download a dedicated desktop application. Access your account settings, navigate to "Apps & Devices," and download the version matching your operating system. The executable file will automatically install Amplenote upon execution.

## Installing the PWA on Windows, macOS, or Linux

Install the Amplenote PWA using Chrome or Brave browsers by clicking the install link that appears after logging in. This action:

- Makes the app accessible via OS Search Spotlight
- Creates a dedicated icon that can be pinned to the dock (macOS)
- Prompts your browser to request data storage permission

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

## Enable Multiple PWA Tabs (Beta Chrome Feature)

This feature allows multiple Amplenote instances simultaneously, such as having the calendar and multiple notes open.

### Enabled Tabbed Windows

1. Type `chrome://flags` in the address bar
2. Search for and enable the two settings shown in the documentation
3. Restart Chrome
4. Navigate to amplenote.com
5. Open Chrome's menu → More tools → Create shortcut
6. Select "Open as tabbed window" and create

Use `Ctrl` + `Page Up/Down` to navigate between tabs quickly.

### Tab Groups

Use Chrome's tab group functionality to visually organize your PWA tabs by category or purpose.

## Updating Amplenote

The app automatically downloads updates, but you must restart it to apply them. An icon appears in the top right corner when updates are available.

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
