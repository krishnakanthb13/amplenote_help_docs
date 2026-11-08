# Plugin API Reference Documentation

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins)

## Overview

Amplenote enables client-side plugins that enhance default functionality across all platforms. A plugin is defined by a single note in a user's account that updates automatically as changes are made.

## Key Documentation Sections

The reference guide includes these main areas:

- **Plugin creation** — Structure requirements for valid plugins
- **Actions** — Available hooks for plugin implementation
- **App Interface** — Interactions with note/task data via `app.*` calls
- **Note interface** — Single-note-specific abstractions
- **Examples** — Common plugin API usage patterns
- **Appendices** — Types, execution environment, markdown content, external libraries, and CORS proxy

## Getting Started Resources

Two particularly helpful pages for developers:

1. "Guide to getting started writing plugins" — assists with creating your first plugin
2. "How to apply markdown formatting" — covers colored text, tables, footnotes, and related functionality

## Recent Updates (2024–2026)

Recent additions include note settings management, clipboard operations, attachment handling, task domain features, and sidebar embed rendering capabilities. The 2025 updates added `app.setNoteSetting`, `app.getNoteSettings`, `app.openEmbed`, and the `onNoteCreated` action.

**October 2026:** `suggestScheduledTasks` now receives `previousSuggestions` (accepted, dismissed, or undecided, along with the scheduled task for accepted ones), and its `check` function is called again after each decision so the plugin can tell Amplenote when it has nothing more to suggest.

The upstream page also keeps a dated changelog of earlier entries (for example `app.context.pluginUUID` in April 2024, `app.context.selectionContent` in March 2024, `app.getNoteImages`/`note.images` in February 2024, `app.deleteNote` and the `prompt` "tags" `limit` in February 2024, `app.setNoteName` in January 2024, `app.alert` action `value` in January 2024, `isRepeating`/`repeat` in October 2023, `app.setSetting` in August 2023, `app.saveFile` in May 2023, and the `app.insertContent` → `app.insertNoteContent` rename with the old name kept as an alias in April 2023).

## Community & Support

Interested developers should email support@amplenote.com from their registered account email address, with feedback also welcomed in the #plugin-atelier Discord channel.
