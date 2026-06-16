# Link to new or existing notes (@ and [[ notation)

> [← Help Index](../00-index.md) · Category: [Notes & Writing](./index.md) · [Source ↗](https://www.amplenote.com/help/double-bracket-note-link-syntax)

## Overview

Amplenote allows users to invoke an "Express Link" dialog by typing `@` (or the legacy `[[`), enabling links to existing notes, note sections, or new notes.

## Simple Note Linking Examples

The simplest approach involves typing `@` followed by the target note's title.

**Key guidelines:**

- Insert `@` before whitespace to link mid-paragraph
- Typing `@` before a word searches for notes containing that word
- Use the phrase-linking hotkey for multi-word note titles

**Bonus tip:** Drag notes from the note list to create references, particularly useful for "Index Notes."

## Note Linking with Tags

### Applying Current Note's Tags to Linked Notes

Start a note link with `@&` to apply tags from your current note to newly created linked notes. This proves valuable when creating related notes within a specific project.

### Declaring Tag Hierarchies

Create tagged note structures using syntax like `@vacations/spicy/Juicy Topic`. Multiple tags can be added by separating them with commas.

**Navigation shortcuts:**

- `Ctrl-Space`: Jump into newly linked reference
- `Cmd-,` (macOS) or `Ctrl-,` (PC): Jump back to previous note
- `Cmd-g` (macOS) or `Ctrl-g` (PC): Invoke history menu

## Linking to Sections Within Notes

Enter `#` in the linking dialog to target specific sections. After creating the link, hovering over the resulting Rich Footnote displays the section's full contents.

**Special syntax:** Type `@#` to link to sections within the current note—particularly helpful for task context.

### Example: Section Links for Task Context

When creating tasks, append `@#` and select the relevant section to preserve surrounding research context accessible from Tasks or Calendar View.

## Linking to Tasks

As of late 2024, users can link directly to tasks, not just notes. Detailed information is available on the "Task Dependencies" help page.

## Inserting Sections from Other Notes

Type `@=` to paste content at the cursor position. Options include:

- Press `Enter` to insert entire note content
- Press `#` to select and insert specific sections

## The Phrase-Linking Hotkey

Select text and press `@` to convert it into a note link. If no matching note exists, Amplenote suggests creating one.

**Enhanced option:** Use `Ctrl-Shift-[` to inherit all tags from the current note when linking.

## Extracting Text Selections to Notes

The contextual toolbar enables moving selected text to new or existing notes.

**Text extraction rules:**

- Move to either new or existing notes
- Selected text inserts at target note's beginning
- A link replaces the original selection
- Tag-forwarding rules apply automatically

**Use cases:**

- Maintaining note atomicity
- Converting journal entries to evergreen notes
- Transforming to-do lists into projects
