# Multi-note selections and bulk actions

> [← Help Index](../00-index.md) · Category: [Notes & Writing](./index.md) · [Source ↗](https://www.amplenote.com/help/multi_note_selections_bulk_actions)

## How do I select multiple notes?

There are two primary options to delete groups of notes (aside from plugins).

### Via notes list

To start selecting notes, hover over the note icon to the left of the note title. On hover, the icon changes into a toggle that allows you to select that note.

Once the first note is selected, hovering over other notes will toggle them for selection (regardless of where inside the note preview you put the mouse cursor).

![Hovering over the note icon to the left of the note title to begin selecting](https://images.amplenote.com/0c2a8676-6046-11ed-8694-aec53b9d6759/67b3fa3b-70da-4041-9a83-6b114bb3ecef.png)

![The selection toggle that appears on hover](https://images.amplenote.com/0c2a8676-6046-11ed-8694-aec53b9d6759/a62b2479-a365-4592-99a6-7ceebbc91564.png)

> 💡 **Tip:** "If you click a first note, then scroll down and `Shift-Click` on a later note, the entire span of notes will be selected." Combined with the search filter options, this is a fast way to delete a large swath of notes matching whatever criteria you choose.

![Using Shift-Click to select a span of notes across the list](https://images.amplenote.com/0c2a8676-6046-11ed-8694-aec53b9d6759/909e5caa-4d9e-4291-8e79-5c1eb385a035.gif)

### Via graph view

It's also possible to select and act on notes visually, in Graph View. After filtering the notes you want to delete using the search box and options, you can hold shift and drag a box around a group of notes to select them all. You can then delete the notes, apply a tag, or link to a new note.

## What bulk operations can I use?

Once at least one note is selected, a toolbar will appear at the top of the note list that lets you operate on the selection you've made.

### Bulk add or remove tags from notes

Use the tag option to quickly add or remove a tag from the selected notes. Use the search bar to quickly find the tag you're looking for.

![The tag option in the bulk-action toolbar](https://images.amplenote.com/0c2a8676-6046-11ed-8694-aec53b9d6759/615a785a-f9f3-4f4e-b560-ccfcb117bbd1.png)

![Searching for a tag to apply to the selected notes](https://images.amplenote.com/0c2a8676-6046-11ed-8694-aec53b9d6759/11f8d881-0b35-4b5b-b316-f18b285f730b.png)

"`Shift-Click` on a tag from the list to remove it from all of the notes it was applied to."

#### Bulk add tags using drag-and-drop

Dragging and dropping tags from the sidebar works on multi-note selections too!

### Bulk archive, delete or download notes

You can also bulk-delete, archive or download notes using the options in the top toolbar.

![Bulk archive, delete, or download options in the top toolbar](https://images.amplenote.com/0c2a8676-6046-11ed-8694-aec53b9d6759/8f1fda55-b593-449b-92a4-9ba9d403a3de.png)

## Use cases

### Quickly unarchive multiple notes

In Amplenote, notes are auto-archived after a certain amount of time passes and you don't open those notes.

If you want to undo note auto-archiving for multiple notes at once, you can:

1. Search for `in: auto-archived`, to select all notes tagged with `#auto-archived`
2. Select the first note in the list of results
3. Scroll down and `Shift-Click` to select the last note in the list of results
4. Use the "tag" option in the toolbar and then `Shift-Click` on the tag called `auto-archived` to remove it from all selected notes

### Quickly share multiple notes

Applying a tag to multiple notes in bulk is useful for collaboration on larger projects.

To achieve this, simply:

1. Make sure to create a shared tag
2. Select all of the notes you want to collaborate on
3. Apply the shared tag to those notes

### Bulk operations on tags

You can make tagging corrections in Amplenote by:

- Using common tag operations such as renaming, deleting or merging tags
- Getting more granular using multi-note selections

Using note selections, search queries and bulk-tagging, you can partially merge two tags, branch an existing tag or untangle any tag tree that your knowledge base requires.

#### Partially merge two tags

To partially merge two tags—`interests/travel` and `interests/trips`:

1. Search for `in: interests/trips` to select all "trips" notes
2. Use `Shift-Click` to select all notes that are actually about "traveling"
3. Use the toolbar to apply the `interests/travel` tag to those notes
4. Optionally, remove the `interests/trips` tag if you don't need it anymore

#### Operations on complex tag queries

To remove the `hobbies` tag from all notes that aren't tagged with `music`:

1. Search for `in: hobbies,^music` to select all notes tagged with `hobbies` but not `music`
2. Select all of the notes in the list of results
3. Remove the tag `hobbies` from the note selection

#### Branch a tag into subtags

To create two subtags called `schoolwork/year-1` and `schoolwork/year-2` from `schoolwork`:

1. Search for `in: schoolwork`
2. Select all "Year 1" notes and tag them with `schoolwork/year-1`
3. Search for `in: schoolwork, ^schoolwork/year-1` to exclude all "Year 1" notes
4. Select all results and tag them with `schoolwork/year-2`
5. Optionally, remove the parent `schoolwork` tag from all notes
