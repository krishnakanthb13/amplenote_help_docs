# Link to new or existing notes (@ and [[ notation)

> [← Help Index](../00-index.md) · Category: [Notes & Writing](./index.md) · [Source ↗](https://www.amplenote.com/help/double-bracket-note-link-syntax)

## Overview

Amplenote allows users to invoke an "Express Link" dialog by typing `@` (or the legacy `[[`), enabling links to existing notes, note sections, or new notes.

## Simple Note Linking Examples

The simplest approach involves typing `@` followed by the target note's title.

![How it looks to link to an existing note, or declaring a new note to link into](https://images.amplenote.com/700cfafa-8d91-11ea-b630-a2d7339f9950/1f8b402d-3c31-49c1-968d-ff3b9e18fc7a.gif)

**Key guidelines:**

- Insert `@` before whitespace to link mid-paragraph
- Typing `@` before a word searches for notes containing that word
- Use the phrase-linking hotkey for multi-word note titles

![Inserting @ before whitespace to create a note link mid-paragraph](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/2355736a-9739-41f6-954c-6c4c8e8786a5.gif)

**Bonus tip:** Drag notes from the note list to create references, particularly useful for "Index Notes."

![Dragging a note from the note list to create a reference](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/73b2cb15-4038-4d4a-bb86-adb0613c6787.gif)

## Note Linking with Tags

### Applying Current Note's Tags to Linked Notes

Start a note link with `@&` to apply tags from your current note to newly created linked notes. This proves valuable when creating related notes within a specific project.

![By starting the note link with @&, the tag(s) from the current note will be applied upon pressing enter](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/c4fd8f69-fda4-41b8-a00e-015675a036e0.png)

### Declaring Tag Hierarchies

Create tagged note structures using syntax like `@vacations/spicy/Juicy Topic`. Multiple tags can be added by separating them with commas.

![Linking to a newly created note within the hierarchy](https://images.amplenote.com/700cfafa-8d91-11ea-b630-a2d7339f9950/1a7e7ba7-0c62-479f-a475-07479f293c02.gif)

![Adding multiple tags while creating a note](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/6d2dbffd-9174-4c30-b205-ba82860c5705.png)

**Navigation shortcuts:**

- `Ctrl-Space`: Jump into newly linked reference
- `Cmd-,` (macOS) or `Ctrl-,` (PC): Jump back to previous note
- `Cmd-g` (macOS) or `Ctrl-g` (PC): Invoke history menu

## Linking to Sections Within Notes

Enter `#` in the linking dialog to target specific sections. After creating the link, hovering over the resulting Rich Footnote displays the section's full contents.

![The # key allows you to use the note linking menu to link to a particular section](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/19cdf3fd-8083-4d07-af9b-822de4da7179.gif)

**Special syntax:** Type `@#` to link to sections within the current note—particularly helpful for task context.

### Example: Section Links for Task Context

When creating tasks, append `@#` and select the relevant section to preserve surrounding research context accessible from Tasks or Calendar View.

![The current section will be the default option when opening the selection dialog](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/7ec628c7-7fc5-48a3-abb3-67783f1dae56.gif)

![Viewing the task's note section from Tasks View mode](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/4d87a5df-2418-459f-9833-38154892f83e.png)

## Linking to Tasks

As of late 2024, users can link directly to tasks, not just notes. Detailed information is available on the "Task Dependencies" help page.

## Inserting Sections from Other Notes

Type `@=` to paste content at the cursor position. Options include:

- Press `Enter` to insert entire note content
- Press `#` to select and insert specific sections

## The Phrase-Linking Hotkey

Select text and press `@` to convert it into a note link. If no matching note exists, Amplenote suggests creating one.

![Converting a text selection into a note link with the phrase-linking hotkey](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/d4e550a5-18e2-47da-8e2b-5da92d695054.gif)

**Enhanced option:** Use `Ctrl-Shift-[` to inherit all tags from the current note when linking.

![Using the Ctrl-Shift-[ hotkey links to a new or existing note, adding all of the tags](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/166d4fef-9975-40e6-b940-85b397af477a.gif)

## Extracting Text Selections to Notes

The contextual toolbar enables moving selected text to new or existing notes.

![Contextual toolbar buttons for extracting a text selection to a Rich Footnote or separate note](https://images.amplenote.com/c1d821d0-fad2-11ea-a5bc-f200a12bf340/d489af97-2ce1-492d-bfc1-2d350692a16c.png)

**Text extraction rules:**

- Move to either new or existing notes
- Selected text inserts at target note's beginning
- A link replaces the original selection
- Tag-forwarding rules apply automatically

**Use cases:**

- Maintaining note atomicity
- Converting journal entries to evergreen notes
- Transforming to-do lists into projects
