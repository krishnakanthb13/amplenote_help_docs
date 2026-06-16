# "Jots" — what are they vis-a-vis "Notes"?

> [← Help Index](../00-index.md) · Category: [Capture: Jots & Amplecap](./index.md) · [Source ↗](https://www.amplenote.com/help/jots)

## What is a "Jot" and how is it different from a "Note"?

Writing in Amplenote happens primarily between two modes provided in the left sidebar: "Jots" and "Notes."

In Amplenote, every jot is a note and vice versa. The purpose of Jots mode is "to facilitate simple, quick idea capture," serving as the first step in the "Idea execution funnel."

Jots excels when creating first drafts or using a scratchpad for immediate problems. Notes mode is designed for polishing rough ideas into shareable, professional content with its formatting toolbar, multiple tag capabilities, and detailed action menus.

![Notes mode with its formatting toolbar and tagging](https://images.amplenote.com/43301082-fb67-11ea-a4f3-1a263ad550a8/eb8599f1-7903-4219-8601-67e6a268f91e.png)

## Purpose of Jots mode

The purpose of "Jots" is to facilitate simple, quick idea capture. When sketching out ideas and connections, Jots mode provides a zero-clutter, distraction-free writing space. It lacks the formatting toolbar found in Notes mode; instead, users apply formatting through keyboard shortcuts or markdown.

![Single-pane Jots mode (as of September 2020)](https://images.amplenote.com/43301082-fb67-11ea-a4f3-1a263ad550a8/67eddf6c-41b3-4173-8641-c2eadb1b1871.png)

## Using Jots mode

### Creating tasks (and other formatting) in Jots mode

Since Jots mode lacks a formatting bar, use markdown or shortcut keys for formatting. You can select text to see formatting options via a toolbar added in December 2021.

To create a task, type `[]` followed by the task content. Users can leverage the Keyboard Shortcuts & Markdown Syntax Examples for additional formatting options.

![Select text written in your jot to see the available formatting options.](https://images.amplenote.com/43301082-fb67-11ea-a4f3-1a263ad550a8/c8a35bdc-286c-4d48-a81a-d9062b70ce4b.gif)

### Linking to new notes from Jots mode

Use the `@` syntax to create links to new or existing notes. Links automatically receive the currently selected tag unless prevented through settings.

![Note linking from Jots mode](https://images.amplenote.com/43301082-fb67-11ea-a4f3-1a263ad550a8/4103c444-696b-4e35-98f2-b96d829fcbb7.png)

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

![Annotated two-pane view showing the #daily-jots tag](https://images.amplenote.com/43301082-fb67-11ea-a4f3-1a263ad550a8/6bb5d309-da17-459e-ba16-3052594213da.png)

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

![Brainstorming on a topic within a tag hierarchy in Jots mode](https://images.amplenote.com/43301082-fb67-11ea-a4f3-1a263ad550a8/7a972a11-3508-442f-8e8d-5d901e2682cc.png)
