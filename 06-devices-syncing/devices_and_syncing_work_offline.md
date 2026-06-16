# Does Amplenote work offline?

> [← Help Index](../00-index.md) · Category: [Devices & Syncing](./index.md) · [Source ↗](https://www.amplenote.com/help/devices_and_syncing_work_offline)

## Working Offline in Amplenote

Amplenote was built from the ground up as an offline-first application. Even if you have no connection (or a spotty connection) to the internet, Amplenote can still be used as either an [installed PWA](https://www.amplenote.com/help/installing_amplenote_macos_windows_linux_ios_android) or through our native mobile apps.

## Ensuring offline availability on desktop

The easiest way to ensure that offline mode will work via desktop is to install the Amplenote app as a PWA, as [described in our instructions](https://www.amplenote.com/help/installing_amplenote_macos_windows_linux_ios_android). Once the app has been installed, your browser will grab and cache what's known as a "Service worker," that allows Amplenote to continue to function even when you're not later connected to the internet.

Assuming you do not log out, this Service Worker should remain cached indefinitely, allowing you Offline access even through a browser restart cycle.

## Knowing when you're offline

If you're offline, the sync icon for your note will change to orange, as well as the status icon in the top bar of the app.

![A user who is currently disconnected from wifi will see a status icon like the one pictured](https://images.amplenote.com/9be4660e-3994-11eb-ad2d-ae6cdc088504/4927f6bd-b5ed-4435-9225-e3d7363dd926.png)

## What content can be opened?

Anything that has been previously downloaded. When you first log in to Amplenote on a new device, we begin downloading and caching your existing notes list. When notes have not yet been cached, they have an icon that points down next to the note title, and no note content preview. Once you can see a note's preview, you can open and edit it offline.

## Actions available offline

When you're offline, you can still do pretty much anything:

- Read notes
- Edit/write notes
- Upload attachments
- Use Quick Open
- Use search
- Create tasks
- Add tags
- Check off tasks
- Etc.

Unless it is specifically in the "Actions unavailable offline" list, the feature should work.

When you upload an image or PDF offline, we store it locally and then push it to the Amplenote server next time you get a working internet connection.

## Actions unavailable offline

There are a few actions in Amplenote that require a connection to the server:

- Sharing or publishing a note
- Encrypting a new Vault Note (we need to ensure that your password token matches your previous answer)
- Viewing or changing Amplenote account settings

## Sync icons

Our goal is have notes sync reliably with no work on behalf of the user, and to remain well-supported even if you are working offline or with limited bandwidth.

The icon near the top right of the screen indicates Amplenote's current sync state. The sync states are defined as follows:

| Icon | Status |
|------|--------|
| Green checkmark | Sync complete. Your note is up to date across all your devices. |
| Circular arrows | Syncing in progress. |
| Circular arrows with refresh | Refreshing note. Amplenote is comparing your note in the app to the content in the server, and merging the two. |
| Orange exclamation | Amplenote is not able to access your content in the server. Typically, this indicates you are not connected to the internet. |
| Orange triangle | You have made changes to your note(s) since Amplenote was last able to access the server. Amplenote will merge these changes with the server as soon as you reconnect to the internet. |

![Sync complete. Your note is up to date across all your devices.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/9afa8a82-566e-4571-b812-65f8ce780baf)

![Syncing in progress.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/b63f095d-cb4d-4bd9-832e-7b2f8af87b2a)

![Refreshing note. Amplenote is comparing your note in the app to the content in the server.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/8d9c5374-9ed7-4c3a-b224-0359b55eea20)

![Amplenote is not able to access your content in the server.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/59f1e778-6375-4894-be25-6be88b79b9e0)

![You have made changes to your note(s) since Amplenote was last able to access the server.](https://images.amplenote.com/744a092c-0490-11e9-8157-5261ad5891d7/7266f7c2-d4d6-4990-a0a7-b88729890fb4)
