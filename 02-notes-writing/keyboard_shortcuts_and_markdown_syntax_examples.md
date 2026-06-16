# Keyboard shortcuts (hotkeys) & markdown syntax examples

> [← Help Index](../00-index.md) · Category: [Notes & Writing](./index.md) · [Source ↗](https://www.amplenote.com/help/keyboard_shortcuts_and_markdown_syntax_examples)

## Table of Contents

- 📍 Navigation
- 🔗 Note linking
- 🖥️ Display & Layout
- ✅ Tasks
- 🔮 Evaluation (calculator)
- 🎨 Formatting
- 🤼 Mix and match

---

## 📍 Navigation

### Quick Open

Navigate by note titles, recent notes, or tag hierarchy.

| Windows/Linux | macOS | Function |
|---|---|---|
| `Ctrl-O` | `Cmd-O` or `Ctrl-O` in Safari | Opens and closes the Quick Open menu |
| Arrow keys | Arrow keys | Cycles through visible results |
| `Enter` | `Enter` | Opens the result as the main note |
| `Ctrl-Enter` | `Cmd-Enter` | Opens the result in the Peek Viewer |
| `Tab` | `Tab` | Switches between Note Lookup and Task Lookup |
| `Ctrl-.` | `Cmd-.` | In Task Lookup, shows possible task actions |
| `Esc` | `Esc` | Close the Quick Open menu |

### Open Peek Viewer

| Linux/Windows | Mac |
|---|---|
| `Ctrl-J` | `Cmd-J` |

### Browse Navigation History (backburger menu)

| Linux/Windows | Mac |
|---|---|
| `Ctrl-G` | `Cmd-G` |

Arrow keys and `Enter` to navigate this menu using the keyboard.

### Open an Existing Note or PDF Inside the Peek Viewer

| Linux/Windows | Mac |
|---|---|
| `Ctrl-Click` on a note or note link; `Ctrl-Enter` when in Quick Open | `Cmd-Click` on a note or note link; `Cmd-Enter` when in Quick Open |

Notes can also be dragged from the note list and into the Peek Viewer pane.

### Open a New Note Inside the Peek Viewer

| Linux/Windows | Mac |
|---|---|
| `Ctrl-Click` on the "New note" button at the top right corner | `Cmd-Click` on the "New note" button at the top right corner |

### Close Every Other Note in Peek Viewer, Except the Selected Note

| Linux, Windows & Mac |
|---|
| `Shift-Click` on the "x" button in the note open in Peek Viewer |

### Move from/to Note Title to the Note Tags Section

| Linux, Windows & Mac |
|---|
| `Tab` to move from the note title to the tag section |
| `Shift-Tab` to move from the note title to the tag section, if the cursor is at the start of the note body |

### Move to Note Tags Section from Anywhere Inside the Note Body

| Linux/Windows | Mac |
|---|---|
| `Ctrl-Alt-T` | `Ctrl-Opt-T` |

### Create a New Note

| Linux/Windows | Mac |
|---|---|
| `Ctrl-Alt-N` | `Cmd-Alt-N` |

### Visit Link at Cursor

| Linux/Windows | Mac |
|---|---|
| `Ctrl-Shift-.` (think Ctrl->); `Ctrl-Space` | `Cmd-Shift-.` (think Cmd->); `Ctrl-Space` |

### Return to the Previous Note

| Linux/Windows | Mac |
|---|---|
| `Ctrl-Shift-,` (think Ctrl-<) | `Cmd-Shift-,` (think Cmd-<) |

In most cases, you can also use your browser's "back" shortcut:

| Linux/Windows | Mac |
|---|---|
| `Alt-Left arrow` | `Cmd-[` |

### Search for Content Inside a Note

| Linux/Windows | Mac |
|---|---|
| `Ctrl-F` | `Cmd-F` |

---

## 🔗 Note Linking

### Create a New or Link to an Existing Note

| Linux, Mac & Windows |
|---|
| `@` or `Ctrl-[` or `[` (available when text is selected) |

**Markdown syntax:**

```
@Note to be linked to
@a/tagged/note/Note to be linked to
[[Hello world note]]
[[deeply nested/tag hierarchy/Cool new note title]]
[[personal/memories/holidays/December 25, 2020]]
```

### Create or Link to an Existing Note, Transferring All Tags from the Current Note

| Linux, Mac & Windows |
|---|
| `Shift-Ctrl-[` (available when text is selected) |

---

## ↗️ Import/Export

The below only work on the desktop client.

| Windows/Linux | macOS | Action |
|---|---|---|
| `Ctrl-S` | `Cmd-S` | Save the current note as markdown |
| `Ctrl-P` | `Cmd-P` | Save the current note as PDF |
| `Ctrl-Shift-P` | `Cmd-Shift-P` | Open the print dialog for the current note |

---

## 🖥️ Display & Layout

### Increase or Decrease the Number of Panes Shown

| Linux, Mac & Windows |
|---|
| `Alt-[` and `Alt-]` |

### Toggle Right-To-Left Mode

| Linux/Windows |
|---|
| `Ctrl-Shift-X` |

---

## ✅ Tasks

All of the following shortcuts apply when the cursor is inside a task.

**Mnemonic:** The first letter/number of the task context, plus Alt-Shift on Linux/Windows or Ctrl on macOS.

### Create a Task

| Linux, Mac & Windows |
|---|
| `[] ` <-- Start a line with empty brackets followed by space to create a task |

Alternatively, press `Ctrl-Enter` twice on any block. The first press transforms your current block into a bullet list item; the second press transforms it into a task.

| Linux, Mac & Windows |
|---|
| `Ctrl-Enter` |

| Mac |
|---|
| `Cmd-Enter` |

### Task Commands

Use `!` to see available task commands when the cursor is inside a task.

### Mark Task Complete

| Linux, Mac & Windows |
|---|
| `Ctrl-Space` or `!complete` |

Read about task completion in the help documentation.

### Dismiss Task

| Linux & Windows | Mac |
|---|---|
| `Ctrl-Shift-D` or `!dismiss` | `Option-Shift-Space` or `!dismiss` |

Tasks can also be dismissed by holding `Alt` and clicking the task's checkbox.

### Cross Out Task

| Linux, Mac & Windows |
|---|
| `Shift-Ctrl-Space` or `!cross-out` |

Tasks can also be crossed out by holding `Shift` and clicking the task's checkbox.

### Open/Close Task Details

| Linux/Windows | Mac |
|---|---|
| `Ctrl-.` | `Cmd-.` |

`TAB` to navigate between fields; `SPACE` to select.

### Mark Task Urgent

| Linux/Windows | Mac |
|---|---|
| `Alt-Shift-U` | `Ctrl-U` |

| Linux, Mac & Windows |
|---|
| `!urgent` |

### Mark Task Important

| Linux/Windows | Mac |
|---|---|
| `Alt-Shift-I` | `Ctrl-I` |

| Linux, Mac & Windows |
|---|
| `!important` |

### Mark Task Duration

| Linux/Windows | Mac |
|---|---|
| `Alt-Shift-[First number]` | `Ctrl-[First number]` |

| Linux, Mac & Windows |
|---|
| `!duration` |

### Create a New Line in a Task

| Linux, Mac & Windows |
|---|
| `Shift-Enter` |

### Paste Into a Task

| Linux/Windows | Mac |
|---|---|
| `Ctrl-Shift-V` | `Cmd-Shift-V` |

### Expand or Collapse Sub-tasks

| Linux, Mac & Windows |
|---|
| `Ctrl-,` |

Works when cursor resides within the parent task.

---

## 🔮 Evaluation (Calculator)

### Math Calculation

```
{1+1}
{pi*10**2}
```

### Date and Time Calculation

**Relative date calculation:**

```
{Today}
{Tomorrow}
{Yesterday}
```

**Absolute dates:**

```
{Monday}
{The weekend}
{September}
{October 31st}
{Oct 31}
```

**Past and future dates:**

```
{Next monday}
{Last week}
{Next year}
{In 14 days}
{A month ago}
```

**Time calculation:**

```
{Now}
{10 minutes ago}
{In three hours}
{9 pm}
{21:30}
```

**Date and time calculation:**

```
{Today at 8pm}
{Tomorrow at 10:45}
{Tuesday 22:00}
{Mar 12 8am}
```

💡 **Quick tip:** Date and time calculation works in the `Ctrl-O` Quick-open menu too!

### Plugin Command Menu

Type `{` followed by the name of the plugin to see all of that plugin's available actions. Press `Enter` to run it.

---

## 🎨 Formatting

### Rich Footnotes/Links

| Linux/Windows | Mac |
|---|---|
| `Ctrl-K` | `Cmd-K` |

**Markdown syntax:**

```
[Link](https://www.amplenote.com)
```

When no text is selected, `Ctrl-K` brings up an extended Rich Footnote menu. When text is selected, it jumps directly to the link menu. To remove a footnote, press `Ctrl-K` with the cursor positioned on the footnote's text.

### Jump In or Out of Rich Footnotes

| Linux, Mac & Windows |
|---|
| `Tab` |

### Other Text Formatting

| Windows/Linux | macOS | Action |
|---|---|---|
| `:emoji-name:` | `:emoji-name:` | Insert an emoji with the emoji browser |
| `[] Task name` | `[] Task name` | Insert a task at the current position |
| `Tab` | `Tab` | Indent a list/task item |
| `Shift-Tab` | `Shift-Tab` | Unindent a list/task item |
| `Shift-Ctrl-Up` / `Shift-Ctrl-Down` | `Shift-Ctrl-Up` / `Shift-Ctrl-Down` | Move a list/task item up or down |
| `^highlighted text^` / `Ctrl-H` | `^highlighted text^` / `Cmd-H` | Apply highlight formatting |
| `* bullet point` / `- bullet point` | `* bullet point` / `- bullet point` | Insert a bullet point at the current position |
| `Ctrl-Enter` | `Ctrl-Enter` | Strikethrough a task/list item |
| `Ctrl-,` | `Ctrl-,` | Expand/collapse a task/list/heading |
| `1. numbered list` | `1. numbered list` | Insert a numbered item list at the current position |
| `> block quote` | `> block quote` | Insert a block quote at the current position |
| `` `code snippet` `` / `` Ctrl-` `` | `` `code snippet` `` / `` Ctrl-` `` | Insert a code snippet |
| ``` ``` | ``` ``` | Insert a code block |
| `~strikethrough~` | `~strikethrough~` | Insert strikethrough text |
| `Ctrl-Z` / `Shift-Ctrl-Z` | `Cmd-Z` / `Shift-Cmd-Z` | Undo/Redo editor operations |
| `Ctrl-B` / `*bold text*` | `Cmd-B` / `*bold text*` | Format text as **bold** |
| `Ctrl-I` / `_italic text_` | `Cmd-I` / `_italic text_` | Format text as _italic_ |
| `Ctrl-/` | `Cmd-/` | Clear formatting of selected text |

### Header 1

| Linux, Mac & Windows |
|---|
| `Shift-Ctrl-1` |

**Markdown syntax:**

```
# text
```

### Header 2

| Linux, Mac & Windows |
|---|
| `Shift-Ctrl-2` |

**Markdown syntax:**

```
## text
```

### Header 3

| Linux, Mac & Windows |
|---|
| `Shift-Ctrl-3` |

**Markdown syntax:**

```
### text
```

### Convert Header to Standard Paragraph

| Linux, Mac & Windows |
|---|
| `Shift-Ctrl-0` |

### Horizontal Line

| Linux & Windows | Mac |
|---|---|
| `Shift+Ctrl+-` | `Shift+Cmd+-` |

**Markdown syntax:**

```
---
```

### Create a Hard Break/New Line Inside the Current Block

| Linux, Mac & Windows |
|---|
| `Shift-Enter` |

---

## 🤼 Mix and Match

You can combine _inline_ styling (bold, italic, strikethrough, code snippets, and links/rich footnotes) to _block_ elements (headers, list items, and block quotes).

**Example:** **Here's** an _example_ of _**inline**_ styling `applied` to a block element.

And here's an example of a task with rich footnote.
