# Slash (/) menu: list of available commands

> [← Help Index](../00-index.md) · Category: [Search, Lookup & Navigation](./index.md) · [Source ↗](https://www.amplenote.com/help/slash_command_index_glossary_list_of_available_commands)

## Slash (/) Menu: Direct Cross-Platform Access to Every Feature

### Overview

The forward slash menu in Amplenote provides context-aware commands across all platforms. It's triggered by:

- Entering `/` after a space
- Entering `/` at the beginning of a line
- Selecting text then pressing `/`

The menu adapts based on context—paragraphs show different options than tasks.

---

## 📄 Block Commands

Format current blocks as headings, lists, quotes, or code blocks.

| Command | Function | Shortcut |
|---------|----------|----------|
| `/header 1` | Level-1 heading | Shift+Ctrl/Cmd+1 |
| `/header 2` | Level-2 heading | Shift+Ctrl/Cmd+2 |
| `/header 3` | Level-3 heading | Shift+Ctrl/Cmd+3 |
| `/paragraph` | Normal paragraph | Shift+Ctrl/Cmd+0 |
| `/task list` | Checklist item | `[] task` markdown |
| `/bullet list` | Bullet item | `- text` markdown |
| `/number list` | Numbered list | `1. text` markdown |
| `/quote` | Blockquote | `> text` markdown |
| `/code` | Code block | Triple backticks markdown |

Code blocks support: JavaScript, C, C++, C#, CSS, SCSS, HTML, Python, Ruby, Rust, XML, Plain.

---

## 🎨 Text Formatting Commands

Apply inline formatting to selected text.

| Command | Function | Shortcut |
|---------|----------|----------|
| `/bold` | Bold text | Ctrl/Cmd+B |
| `/italic` | Italic text | Ctrl/Cmd+I |
| `/strikethrough` | Strikethrough | `~text~` markdown |
| `/literal` | Inline code | Backticks markdown |
| `/text color` | Change text color | — |
| `/highlight` | Highlight color | `^text^` markdown |
| `/clear formatting` | Remove all formatting | Ctrl/Cmd+/ |

---

## ⤵️ Insert Commands

### Content Blocks

| Command | Function | Shortcut |
|---------|----------|----------|
| `/new link` | Hyperlink | Ctrl/Cmd+K |
| `/table` | Insert table | Tab at line start |
| `/image` | Upload image/video | — |
| `/expression` | Date/math calculation | — |
| `/now`, `/today`, `/tomorrow`, `/yesterday` | Insert date/time | — |
| `/hard break` | Line break | Shift+Enter |
| `/section separator` | Horizontal rule | Ctrl/Cmd+Shift+- |

### External Content

| Command | Function |
|---------|----------|
| `/link to note` | Connect to another note |
| `/template` | Insert template snippet |
| `/attachment` | Upload file |

---

## 📋 List Item Commands

### Positioning

| Command | Function | Shortcut |
|---------|----------|----------|
| `/indent` | Increase indent | Tab |
| `/outdent` | Decrease indent | Shift+Tab |
| `/move up` | Move item up | Shift+Ctrl+↑ |
| `/move down` | Move item down | Shift+Ctrl+↓ |

### Formatting & Content

| Command | Function | Shortcut |
|---------|----------|----------|
| `/cross` | Strike through | Shift+Ctrl+Space |
| `/task` | Convert to task | Ctrl/Cmd+Enter |
| `/refresh toc` | Update table of contents | — |
| `/collapse` (alias: `/fold`) | Hide children | Ctrl/Cmd+, |
| `/expand` (alias: `/unfold`) | Show children | Ctrl/Cmd+, |
| `/copy` (aliases: `/clone`, `/duplicate`) | Copy to another note | — |
| `/delete` | Delete item | — |

---

## 🗓️ Event Commands (Scheduled Bullet Items)

Bullets with start times become events with these commands:

| Command | Function |
|---------|----------|
| `/start` or `/due` | Set start/due time |
| `/reminder` | Add reminder |
| `/every` (aliases: `/recur`, `/repeat`) | Create recurrence |
| `/duration` | Set event duration in minutes |

---

## ✅ Task Commands

### Completion & Deletion

- `/complete` – Mark complete (Ctrl/Cmd+Space)
- `/cross` – Complete and strike through (Shift+Ctrl+Space)
- `/dismiss` – Mark dismissed, half victory value (Ctrl+Alt/Opt+Space)
- `/delete` – Permanently remove task

### Scheduling & Recurrence

- `/start` – Set start/due time
- `/deadline` – Set deadline (mid-2025 feature)
- `/duration` – Set calendar block duration
- `/hide` (aliases: `/snooze`, `/sleep`) – Hide temporarily
- `/every` – Enable repetition
- `/weekdays` – Repeat Mon-Fri only
- `/weekends` – Repeat Sat-Sun only
- `/schedule` – Hide until start time
- `/reminder` – Add notification

### Moving & Copying

- `/move` – Move to another note
- `/move this task to another section` – Move within note
- `/copy` (aliases: `/clone`, `/duplicate`) – Duplicate to another note

### Mirroring & Linking

- `/mirror` – Create synced copy
- `/mirror existing` – Link to existing mirror
- `/block task` / `/blocked task` – Create blocking relationships
- `/implement goal task` / `/goal task` / `/connect task` – Link to goals
- `/overwrite mirrored content` – Sync all copies
- `/go to source note` – Open original note

### Prioritization & Scoring

- `/max score` – Set to highest-scoring task
- `/reset score` – Clear accumulated score
- `/set task score` – Specify custom score
- `/important` – Toggle important flag (Alt+Shift+I / Ctrl+I Mac)
- `/urgent` – Toggle urgent flag (Alt+Shift+U / Ctrl+U Mac)

### Converting & Sorting

- `/to bullet` – Convert to regular bullet (Ctrl/Cmd+Enter)
- `/to scheduled bullet` – Convert to event
- `/repeat` – Edit recurrence rules
- `/sort` – Sort task list

---

## 🗃️ Table Commands

### Column & Row Adjustments

- `/insert column before`, `/insert column after`
- `/insert row above`, `/insert row below`
- `/delete column`, `/delete row`

### Cell Formatting

- `/border bottom` / `/border left` / `/border right` / `/border top`
- `/clear borders` – Remove all borders
- `/cell text color` – Change text color
- `/cell fill color` – Change background color
- `/clear cell formatting` – Remove formatting
- `/align left` / `/align center` / `/align right`

### Select & Adjust

- `/select column` and `/select row`
- `/sort by column` – Sort by column content
- `/fit column` – Resize to fit content
- `/clear column width` – Remove fixed width
- `/toggle full width` – Expand/collapse table

---

## 👥 Collaboration & Sharing Commands

- `/invite` (alias: `/add`) – Share note with collaborators
- `/publish` – Generate public viewing link

---

## 🧩 App Control & Plugin Commands

### Built-in Controls

- `/full` – Toggle full-width note view
- `/autolink` – Link capitalized words matching note names
- `/explore links` – View graph of connected notes/tasks

### AI & Plugin Features

- `/continue` – Install Ample Copilot plugin
- `/generate`, `/thesaurus`, `/rhyme` – AmpleAI content assistance
- `/draw`, `/paint` – Excalidraw visualization
- `/kanban` – Format tasks as Kanban board
- `/math`, `/latex` – Insert mathematical content
- `/mindmap` – Create mind map visualization
- `/pomodoro`, `/focus` – Start focus session
- `/readwise` – Sync Readwise book highlights
- `/remind` – Schedule note review reminder
- `/youtube` – Embed YouTube videos

---

## 💡 Tips for Using Slash Menu

- **Context-awareness:** Menu filters based on cursor location
- **Short aliases:** Use fuzzy matching (e.g., `/cr` for cross out)
- **Plugin integration:** 100+ plugins extend functionality with their own slash commands
- **Workflow efficiency:** Combined with `!` task commands and keyboard shortcuts enables mouse-free operation
