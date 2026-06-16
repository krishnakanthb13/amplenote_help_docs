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

![Sync complete. Your note is up to date across all your devices.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/9afa8a82-566e-4571-b812-65f8ce780baf)

![Syncing in progress.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/b63f095d-cb4d-4bd9-832e-7b2f8af87b2a)

![Refreshing note. Amplenote is comparing your note in the app to the content in the server, and merging the two.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/8d9c5374-9ed7-4c3a-b224-0359b55eea20)

![Amplenote is not able to access your content in the server.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/59f1e778-6375-4894-be25-6be88b79b9e0)

![You have made changes to your note(s) since Amplenote was last able to access the server.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/7266f7c2-d4d6-4990-a0a7-b88729890fb4)
