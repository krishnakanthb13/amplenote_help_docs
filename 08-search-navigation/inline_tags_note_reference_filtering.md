# Note Reference Filtering (Inline Tags / task tagging)

> [← Help Index](../00-index.md) · Category: [Search, Lookup & Navigation](./index.md) · [Source ↗](https://www.amplenote.com/help/inline_tags_note_reference_filtering)

## What are Note References?

Note References are simply links to other notes. You can create them in several ways:

- Using the `@` symbol (legacy `[[` syntax)
- Drag-and-drop from the note list pane
- Using `Ctrl-[` hotkey to convert selected text into a link

![Creating a note reference with the @ linking syntax](https://images.amplenote.com/700cfafa-8d91-11ea-b630-a2d7339f9950/1f8b402d-3c31-49c1-968d-ff3b9e18fc7a.gif)

![Creating a reference by drag-and-drop from the note list](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/73b2cb15-4038-4d4a-bb86-adb0613c6787.gif)

![Using the Ctrl-[ hotkey to link selected text](https://images.amplenote.com/23f25aae-fad1-11ea-a5bc-f200a12bf340/d4e550a5-18e2-47da-8e2b-5da92d695054.gif)

## What are Inline Tags?

"Inline Tags" and "Note References" are interchangeable terms. They function identically to Note References but allow you to tag specific portions of notes rather than entire notes. Traditional tags remain unchanged and apply only at the note level.

Example: `check_box_outline_blank Refund concert tickets (@low-effort)`

## How do I create an Inline Tag?

Simply create a link to a note using the `@` syntax or linking menu. You can either:

- **Add an existing Inline Tag** by searching for the note through the linking menu
- **Create a new inline tag** by typing a name that doesn't exist yet; the system offers to create the note

**Tip:** Using the `~` sign before a link (e.g., `~@journal`) prevents automatic tagging of newly created notes.

## Why do Note References work as Inline Tags?

Both Traditional and Inline Tags share:

1. A mechanism for effortlessly applying existing tags through suggestions and auto-completion
2. The ability to filter notes and tasks using tag combinations

![Traditional Tags (left) and Inline Tags (right)](https://images.amplenote.com/62ccdd04-76da-11ec-b1d8-1eca04f4fc71/2a16047c-a389-4d82-a64e-85173653a9aa.gif)

![Traditional Tags (left) and Inline Tags (right)](https://images.amplenote.com/62ccdd04-76da-11ec-b1d8-1eca04f4fc71/11946adb-87cb-4d10-9c05-48fde69f0498.gif)

![Traditional Tags (left) and Inline Tags (right)](https://images.amplenote.com/8f50f93a-fae1-11ea-95c1-f200a12bf340/a41b1ae3-8c41-40a7-9c23-94a32fa549ab.png)

![Traditional Tags (left) and Inline Tags (right)](https://images.amplenote.com/62ccdd04-76da-11ec-b1d8-1eca04f4fc71/5400cba4-dc8f-4d3f-828d-3f5fef31e84c.png)

## How to filter to-dos by Note References?

"A separate help page dedicated to explaining all the ways that tasks can be filtered by project and note reference" exists for detailed instructions.

## How to filter arbitrary blocks by Note References?

Creating a link generates a **Backlink** (reciprocal link). View backlinks by scrolling to the bottom of any note and clicking the `Backlinks` tab. This displays all places linking to that note.

To filter backlinks:

- Click the Filter icon in the top right of the Backlinks tab
- Apply filters by selecting notes
- `Shift-Click` shows backlinks that exclude the selected note

You can also filter by the source note's tags.

![A screenshot of the Backlinks tab for a note called '🏊 Project: Take Swimming lessons'.](https://images.amplenote.com/62ccdd04-76da-11ec-b1d8-1eca04f4fc71/11038207-62e8-425e-b0af-cfa27eafc6a2.png)

![Filtering backlinks by @Andrew using the Backlinks filter](https://images.amplenote.com/62ccdd04-76da-11ec-b1d8-1eca04f4fc71/ab841da0-7d5a-428d-a168-36970d1b291a.png)

## How is this useful?

### Setting up Task Contexts

Task Contexts help manage overwhelmingly large to-do lists by adding metadata signaling what action is needed and what's required to complete it. Common context candidates include:

- **Places:** @home, @office, @anywhere
- **Activities:** @phone-call
- **Energy levels:** @low-energy, @high-energy
- **People:** @person-name

Context tagging enables filtering tasks based on your current situation, reducing overwhelm by showing only actionable items.

### Linking and categorizing ideas

Inline Tags apply to any block type (paragraphs, bullet points, headings). When referencing a note in a block, everything beneath that block becomes tagged with that reference.

**Key principle:** Tagging a bullet or task also tags all sub-bullets/sub-tasks; tagging a heading tags all contained blocks.

**Example workflow:** Write meeting notes directly in your Daily Jot, tagging with both the meeting type (`Planning meeting`) and participant (`@Richard`). Later, access the Backlinks tab for "Planning meeting" to view all instances, then filter by `@Richard` to see only meetings with that person.

![Creating a separate meeting notes note](https://images.amplenote.com/62ccdd04-76da-11ec-b1d8-1eca04f4fc71/e4478d53-6f03-418e-ad1a-a2d2bbfc34de.png)

![Tagging a bullet point with "Planning meeting" and "@Richard" in a Daily Jot](https://images.amplenote.com/62ccdd04-76da-11ec-b1d8-1eca04f4fc71/fde57caf-d26c-42e3-8c6d-0c334cbfa12a.png)

![The Backlinks tab for a note called 'Planning meeting'](https://images.amplenote.com/62ccdd04-76da-11ec-b1d8-1eca04f4fc71/6a6539ca-2478-4603-81b0-6eb696127af3.png)

![Filtering backlinks to show planning meetings with Richard](https://images.amplenote.com/62ccdd04-76da-11ec-b1d8-1eca04f4fc71/f857ff3b-e0d4-4625-8fc7-31fd9c038781.png)

## Traditional vs Inline Tags?

**Choose Traditional Tags for:**

- Notes you want to share with groups (via shared tags)
- Delimiting domains of applicability (e.g., `#blog`, `#todos`)

**Choose Inline Tags for:**

- Tagging individual tasks for useful categories (e.g., "Next," "On hold")
- Separating to-dos into projects
- Logging date-sensitive information
- Registering references to people, concepts, or subjects of regular interaction

**General rule:** "Traditional tags should be general, Inline Tags should be specific." Use Inline Tags for specific people's names (`@Wayne`, `@Beatrice`) and a Traditional Tag to group them (`#people`).
