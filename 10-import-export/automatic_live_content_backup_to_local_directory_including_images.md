# Automatic (live) backup for note content & attachments

> [← Help Index](../00-index.md) · Category: [Import & Export](./index.md) · [Source ↗](https://www.amplenote.com/help/automatic_live_content_backup_to_local_directory_including_images)

## Overview

Amplenote Desktop app users can select a directory for automatic local backup of all note content, images, PDFs, and media files.

## How to setup automatic backups

1. Download the Amplenote Desktop app
2. Click "Settings" under the "Amplenote Desktop" menu
3. Choose a backup directory
4. Amplenote will download any unrefreshed note content and write each note as a markdown file using the note's unique identifier as the filename

![Choosing a backup directory in Ample Desktop settings](https://images.amplenote.com/fdd718cc-d826-11ef-b630-2badab5b1c7d/cf3702ac-6eb6-454f-9d64-6d3fa67a0f02.png)

## Backing up images, video and PDFs

All assets uploaded to Amplenote are included in automatic backups. Assets are stored in a `media` subdirectory of the main backup directory, with subdirectories corresponding to note identifiers.

## Differences between automatic backup and export

| Feature | Automatic Backup | Export |
|---------|-----------------|--------|
| Availability | Desktop app only | Desktop and web app |
| Format | Individual files in directory | Single zip file |
| File naming | Note unique identifier | Note title |
| Vault Notes support | Yes | No |

![Export uses the note title as the first field of the file name](https://images.amplenote.com/fdd718cc-d826-11ef-b630-2badab5b1c7d/52e3835d-1298-41bb-84c9-cf090665934a.png)

The backup system uses unique identifiers rather than titles to "preserve cross-note links" and avoid broken references during note renames.

## How to get the unique identifier (UUID) for a note

1. Click the triple dot in the upper-right corner of a note
2. Choose "View all details" or press Shift-Ctrl-O
3. View or copy the UUID from the details panel

![Open all details for a note](https://images.amplenote.com/fdd718cc-d826-11ef-b630-2badab5b1c7d/c6e7992d-b443-4ae0-9aba-05f4d4e93bdf.png)

![Grabbing the unique identifier for a note](https://images.amplenote.com/fdd718cc-d826-11ef-b630-2badab5b1c7d/c53ca94d-cc47-4495-96e4-d757b6108bf9.png)

## How to change automatic backup directory

Toggle off "Automatic Backup," then re-enable it to select a new directory and avoid ambiguous save states.

## Backup frequency and data currency

Automatic backups occur with the regular server persistence process, typically current within seconds, potentially extending to one minute depending on system load and note change frequency.

## Offline functionality

Backups work offline. Notes created offline use temporary identifiers resolved to final identifiers upon reconnection.

## Link preservation

Markdown exports preserve note and task connections and support "fancy formatting, like Rich Footnotes, colors, and formatting within tables."
