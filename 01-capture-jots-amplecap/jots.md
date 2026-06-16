# "Jots" — what are they vis-a-vis "Notes"?

> [← Help Index](../00-index.md) · Category: [Capture: Jots & Amplecap](./index.md) · [Source ↗](https://www.amplenote.com/help/jots)

## What is a "Jot" and how is it different from a "Note"?

Writing in Amplenote happens primarily between two modes provided in the left sidebar: "Jots" and "Notes."

In Amplenote, every jot is a note and vice versa. The purpose of Jots mode is "to facilitate simple, quick idea capture," serving as the first step in the "Idea execution funnel."

Jots excels when creating first drafts or using a scratchpad for immediate problems. Notes mode is designed for polishing rough ideas into shareable, professional content with its formatting toolbar, multiple tag capabilities, and detailed action menus.

## Purpose of Jots mode

The purpose of "Jots" is to facilitate simple, quick idea capture. When sketching out ideas and connections, Jots mode provides a zero-clutter, distraction-free writing space. It lacks the formatting toolbar found in Notes mode; instead, users apply formatting through keyboard shortcuts or markdown.

## Using Jots mode

### Creating tasks (and other formatting) in Jots mode

Since Jots mode lacks a formatting bar, use markdown or shortcut keys for formatting. You can select text to see formatting options via a toolbar added in December 2021.

To create a task, type `[]` followed by the task content. Users can leverage the Keyboard Shortcuts & Markdown Syntax Examples for additional formatting options.

### Linking to new notes from Jots mode

Use the `@` syntax to create links to new or existing notes. Links automatically receive the currently selected tag unless prevented through settings.

### Renaming Jots

While editing a Jot, press its title to edit it. Changing the title creates a new placeholder jot.

### 🗓️ Creating future daily Jots

Amplenote automatically creates daily Jots. You can manually create ones for future dates using:

`@{Tomorrow}` or `[[{Tomorrow}]]`

Any date expression works. In Notes mode without a selected tag:

`@daily-jots/{Tomorrow}` or `[[daily-jots/{Tomorrow}]]`

For specific tag hierarchies:

`@my/tag/hierarchy/{next friday}` or `[[my/tag/hierarchy/{next friday}]]`

### #daily-jots tag

The default tag when entering Jots mode is `daily-jots`, making it easy to filter notes created in Jots mode.

### How are jots sorted?

Jots follow these sorting rules:

- A date is selected from: the note's title (if dated up to the current day) or the creation date
- Jots sort in descending order by selected date
- For `#daily-jots`, placeholder notes appear for up to the last 7 days without created jots
- For other tags, a placeholder appears only for the current day
- Future Jots display below the current day's jot until becoming current
- Non-dated notes appear below the jot from their creation day
- Renaming today's jot replaces it with a placeholder

### Brainstorming on a topic with Jots

Navigate to any location in your tag hierarchy to ideate there instead of using the default `daily-jots` bucket.
