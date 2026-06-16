# Note Graph View

> [← Help Index](../00-index.md) · Category: [Organize Everything](./index.md) · [Source ↗](https://www.amplenote.com/help/note_graph)

## What is the Graph View mode?

Graph View provides a visual method to browse and organize hundreds or thousands of notes. Access it by clicking the "Graph" button in the interface.

When you create links between notes using bracket syntax, you establish connections. While these have always appeared in each note's "Backlinks" tab, Graph View visualizes them spatially.

Each circle represents a note, with size reflecting content volume. Circle colors derive from applied tags — notes with multiple tags display color gradients. Arrows show link directions, originating from the linking note and pointing to the linked note.

The graph functions as "a map of your notes" and how they interrelate. You can identify patterns like "table of contents" notes with numerous outgoing arrows, or discover isolated nodes — notes lacking any connections — that may warrant action.

## What if I don't have many links between my notes?

Without existing connections, you can build them using:

- The Unlinked References tab to find overlooked connections
- The AutoLink Plugin for automatic link application

## Navigation

Navigation controls appear on the right side. Mouse/trackpad allows zooming via scrolling and movement through click-and-drag.

### Keyboard shortcuts / hotkeys

| macOS | Windows/Linux | Effect |
|-------|---------------|--------|
| `c` | `c` | Center view on graph/selected notes |
| `Space` | `Space` | Zoom to fit all visible nodes |
| `Shift-Click` and drag | `Shift-Click` and drag | Select multiple nodes |
| `Cmd-Click` on node | `Ctrl-Click` on node | Open note in Peek Viewer |
| `m` when note selected | `m` when note selected | Enter note linking mode |

## Searching and filtering the note graph

By default, the graph loads up to 1,000 notes; adjust this via the settings menu. Additional filtering options include:

- Date range filtering for notes updated within specified periods
- Search bar (switchable between full and title search)
- Group and tag filtering options
- Query syntax like `in: ^work` to exclude categories

From various app locations, you can jump directly to filtered graph views through note options menus, the Backlinks tab, search bar, or Jots Mode.

## Note selection and batch operations

### Manually selecting nodes

Hold `Shift` while clicking and dragging to select or deselect multiple notes for batch operations. Use `Shift-Click` on individual nodes for fine-tuning.

### Selecting notes under a certain tag

Click a tag name to select all visible notes bearing that tag.

### Selecting incoming/outgoing links

When a note is selected, two buttons enable quick selection of:

- All notes linking to the selected note
- All notes the selected note links to

### Batch note operations

With multiple notes selected, you can apply/remove tags, download, delete, archive notes, or create connections using standard Amplenote note operations.

### Use case example: Select and fine-tune notes to be deleted

Filter for matching search terms, select all results, deselect false positives, then apply deletion via the multi-select toolbar.

### Use case example: Apply a common tag to related notes

When a note has numerous outgoing links, select all referenced notes and batch-apply a common tag.

## Introducing Note Emojis 😎

The first emoji in a note's title becomes its dedicated emoji icon in Graph Mode. To add or change it, select the note and tap the icon left of the title.

Common uses include: 💼 for work notes, 📋 for reviews, 🎶 for music hobbies.

## Visualize note links & connections

Nodes represent notes; arrows represent links with direction originating from the linking note. Isolated nodes have no connections.

Highlight unlinked notes via the note count menu on the left, or toggle visibility in settings.

When selecting a note, connected notes highlight with incoming and outgoing link details displayed.

## Creating new links & the Note Linking mode

### When two or more notes are selected

Use the note linking menu to designate a target note. Press `Enter` to link that target to all selected notes.

### When a single note is selected

Press `m` or use the nav button to enter Note Linking mode. Clicking nodes adds their links to the initially selected note; clicking again removes the connection.

## Interaction with Peek Viewer

`Ctrl-Click` or `Cmd-Click` nodes to preview in Peek Viewer. From Peek Viewer's options menu, jump directly to that note on the Graph.

### Peek Viewer & Graph View: A power couple for capturing insight 👯

Keep a note open in Peek Viewer while browsing Graph View to capture insights generated during navigation and reflection.

## Troubleshooting

### I cannot interact with nodes in Graph Mode using Brave browser

Disable "Shields" for amplenote.com in Brave to resolve interaction issues.

## On the horizon

Planned 2024 expansions include native mobile Graph View and miniature graph previews in Peek Viewer.
