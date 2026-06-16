# How does syncing work?

> [← Help Index](../00-index.md) · Category: [Devices & Syncing](./index.md) · [Source ↗](https://www.amplenote.com/help/devices_and_syncing_how_syncing_works)

## Overview

Amplenote automatically detects changes to notes and synchronizes them across all devices. The application was built from the ground up to avoid merge conflicts common in older note-taking apps.

The stated objective is to "have notes sync reliably with no work on behalf of the user, and to remain well-supported even if you are working offline or with limited bandwidth."

## Sync Status Indicators

A status icon near the top right of the screen displays the current sync state:

| Icon | Status | Meaning |
|------|--------|---------|
| Green checkmark | Sync complete | "Your note is up to date across all your devices." |
| Circular arrows | Syncing in progress | Changes are being transmitted |
| Circular arrows (refresh) | Refreshing note | "Amplenote is comparing your note in the app to the content in the server, and merging the two." |
| Orange exclamation | Offline / No access | "Typically, this indicates you are not connected to the internet." |
| Orange triangle | Pending sync | "You have made changes to your note(s) since Amplenote was last able to access the server. Amplenote will merge these changes with the server as soon as you reconnect to the internet." |
