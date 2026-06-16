# Comparing the Amplenote PWA to the native desktop app

> [← Help Index](../00-index.md) · Category: [Devices & Syncing](./index.md) · [Source ↗](https://www.amplenote.com/help/compare_native_modern_web_app)

## Overview

Amplenote now provides a native desktop app for Windows, macOS and Linux for paying subscribers, though users with Personal subscriptions must access the service through their browser as a PWA. The article explains the company's rationale for allowing browser-based installation and discusses how perceived weaknesses are addressed.

## What distinguishes a native app?

Historically, native applications offered clear advantages over web apps:

- App is installed to task tray
- Appears in Cmd-Tab application switching
- Offline functionality
- Custom hotkeys for power users
- Enhanced security capabilities
- Push notifications and event reminders
- Stays resident in memory for instant capture
- Smoother visual effects (subjective)
- Faster performance (subjective)

The article notes that technological evolution — particularly web workers and service workers — has blurred the distinction. Popular "native" applications like Obsidian and Microsoft VS Code actually use Electron, which "bundles a website into a pre-packaged Chrome browser."

## How does Amplenote stack up as a native app?

### 1. App is installed to task tray

Users can install Amplenote in "less than a minute" and pin it for easy access with an Amplenote icon in the task tray.

### 2. Cmd-Tab application switching

The installed app "shows when tabbing between apps" like standard native applications.

### 3. Offline functionality

"Amplenote was designed as an offline-first app." Users can create notes, search existing ones, and upload media without connectivity. Exceptions include calendar syncing and OCR features requiring internet access.

### 4. Hotkeys for power users

Amplenote offers extensive keyboard shortcuts and supports "interesting date & math calculations."

### 5. Security

All notes receive "encryption at rest, encrypted in transit" with "industry-best practices" security. The platform also offers Vault Notes, which provides "note content that can't be decrypted even with full access to the Amplenote database."

### 6. Push notifications and event reminders

Chrome PWA notifications are available after installation, enabling "event notifications possible with a standard desktop app."

### 7. Instant capture on desktop

The Amplecap browser extension's Omnicapture feature allows "instant" idea capture "with a single hotkey."

### 8. Smoother/refined visual effects

The founding team "came from a video game background" and focuses on "visual effects" that "reaffirm user actions, and make the app experience more satisfying."

### 9. Performance speed

A 2021 performance study by NoteApps.info comparing 22 note-taking applications found "no measurable distinction between which apps performed best between 'native app,' 'web app,' and various hybrid apps."

## Where native still matters (mobile and iPad)

The distinction between native and web applications remains significant on mobile platforms. Amplenote accordingly "offers native apps for iOS, Android, and iPad."

---

## Links Referenced

- [Native desktop system requirements](https://www.amplenote.com/help/native_desktop_system_requirements)
- [Installing Amplenote guide](https://www.amplenote.com/help/installing_amplenote_macos_windows_linux_ios_android)
- [Web workers](https://en.wikipedia.org/wiki/Web_worker)
- [Keyboard shortcuts and markdown syntax](https://www.amplenote.com/help/keyboard_shortcuts_and_markdown_syntax_examples)
- [Calculations feature](https://www.amplenote.com/help/calculations)
- [Security design details](https://www.amplenote.com/help/amplenote_security_design)
- [Vault Notes overview](https://www.amplenote.com/help/vault_notes_overview)
- [Amplecap browser extension guide](https://www.amplenote.com/help/amplecap_browser_extension_guide#Omnicapture)
- [NoteApps.info performance report](https://www.noteapps.info/state_of_note_apps_performance_2021_with_charts)
- [Devices and syncing](https://www.amplenote.com/help/devices_and_syncing_download_apps#How_do_I_download_mobile_apps?)
- [Offline functionality](https://www.amplenote.com/help/devices_and_syncing_work_offline)
