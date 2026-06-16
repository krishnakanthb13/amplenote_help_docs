# Creating a bespoke Kanban Board

> [← Help Index](../00-index.md) · Category: [Use Cases](./index.md) · [Source ↗](https://www.amplenote.com/help/bespoke_kanban_board)

## New as of October 2024

A community-submitted plugin enables Kanban boards inside Amplenote: **Kanban by Krishna Kanth B**

---

## Manual Workaround for Emulating a Kanban Board

Amplenote lacks native Kanban board support, but users can create a functional equivalent that provides "a quick overview of your tasks" with drag-and-drop capability.

![Emulating a Kanban Board in Amplenote with configurable states; tasks can be quickly drag-and-dropped to a new state](https://images.amplenote.com/5494c6f4-268d-11ec-9677-c64a96ade4ff/279bc564-d339-4c18-b457-7ef447575a20.gif)

### Step #1: Create Your Task States

For each workflow state, create a dedicated note. This example uses three columns: `NEW`, `IN PROGRESS`, and `DONE` (customizable).

**1.1: Title Your State-Notes**

Create one note per state with numbered titles in desired column order:
- `1-NEW`
- `2-IN PROGRESS`
- `3-DONE`

Numbers ensure proper sorting during later configuration.

**1.2: Tag Your State-Notes**

Apply a consistent tag like `todo/kanban` to all state-notes for easy filtering.

**1.3: Populate with Tasks**

Add "at least one task to each state, because notes with no tasks don't show up in Tasks view."

### Step #2: View Your Kanban Board

1. Navigate to Tasks Mode
2. Click on your Kanban tag (`todo/kanban`)
3. Add the tag as a Tag Shortcut for quick access
4. Group tasks by source note
5. Sort tasks by source note, alphabetically

![Grouping tasks by source note in Tasks Mode](https://images.amplenote.com/5494c6f4-268d-11ec-9677-c64a96ade4ff/43ec04b6-5618-47fe-9707-3058851fd7f1.png)

![Sorting tasks by source note alphabetically](https://images.amplenote.com/5494c6f4-268d-11ec-9677-c64a96ade4ff/0f4991ca-cc15-4c7a-a363-58300b0d76f8.png)

![The configured Kanban board viewed in Tasks Mode](https://images.amplenote.com/5494c6f4-268d-11ec-9677-c64a96ade4ff/9ce7100b-e317-40ce-a6f2-104336783645.png)

### Step #3: You're Done!

Features available:
- Use drag-and-drop to transition tasks between states
- Add details using Rich Footnotes and formatting
- Add state-notes to Task Domains for time-blocking
- Share state notes with colleagues for collaborative access

### Optionally: Filter by Project

Use Note References to filter the Kanban board by project. When creating tasks, reference the relevant project note. In Tasks Mode, apply a secondary filter to view only project-specific tasks.
