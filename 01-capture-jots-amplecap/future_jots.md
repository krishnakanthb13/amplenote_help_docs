# Creating future daily jots

> [← Help Index](../00-index.md) · Category: [Capture: Jots & Amplecap](./index.md) · [Source ↗](https://www.amplenote.com/help/future_jots)

## What is a "Jot" and how is it different from a "Note"?

In Amplenote, every jot is a note and vice versa. The purpose of Jots mode is **to facilitate simple, quick idea capture**. Jots work best for rough drafts and scratchpads, while Notes mode is designed for polished, shareable content with formatting toolbars, multiple tags, and detailed action menus.

## Purpose of Jots mode

The primary purpose of Jots is providing "a zero-clutter, distraction-free place to write." It lacks the formatting toolbar found in Notes mode and requires keyboard shortcuts or markdown formatting for text styling.

## Using Jots mode

### Creating tasks (and other formatting) in Jots mode

Create tasks by typing `[]` followed by your task text. For example: `[] buy groceries`. You can also use markdown or keyboard shortcuts for formatting. A formatting toolbar was added in December 2021—select text to see available options.

### Linking to new notes from Jots mode

Use the `@` syntax for note linking:
- `@{note name}` creates links to new or existing notes
- Links are automatically tagged with the currently selected tag

### Renaming Jots

Press on a jot's title while editing to rename it. Renaming today's jot creates a new placeholder jot.

## 🗓️ Creating future daily Jots

Amplenote automatically creates daily jots, but you can manually create future ones. **Two requirements for a manually created note to be a Daily Jot**:

1. Title it with a specific date format: "December 21st, 2021"
2. Assign at least one tag (typically `daily-jots`)

**In Jots mode**, use note-linking syntax:
- `@{Tomorrow}`
- `[[{Tomorrow}]]`

Any date expression works (Tomorrow, next friday, etc.).

**In Notes mode** (with no tag selected):
- `@daily-jots/{Tomorrow}`
- `[[daily-jots/{Tomorrow}]]`

**For specific tag hierarchies**, add the tag path before the date:
- `@my/tag/hierarchy/{next friday}`
- `[[my/tag/hierarchy/{next friday}]]`

## #daily-jots tag

The default `daily-jots` tag is selected when entering Jots mode, making it easy to filter notes created in Jots mode.

## How are jots sorted?

Jots follow these sorting rules:

- Dates are chosen from either the note's title (if dated, up to current day) or creation date
- Jots sort in descending date order
- Placeholder notes appear for up to the last 7 days without a created jot (for `#daily-jots` only)
- Future jots display below the current day's jot until they become current
- Undated notes appear below the jot of their creation day

## Brainstorming on a topic with Jots

You can navigate to any tag in your hierarchy to ideate in Jots mode, not just the default `daily-jots` bucket.
