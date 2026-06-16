# Note Interface: Query or perform actions on a note

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins/note_interface)

## Overview

The Note Interface enables interactions with specific `noteHandle` objects within Amplenote. Notes accessed through this interface may or may not already exist; calling modification functions automatically creates non-existent notes.

## Methods and Properties

### note.addTag
Adds a tag to the note. Returns a boolean indicating success.

### note.attachMedia
Attaches media files (images or videos) to notes. Accepts data URLs and returns the image URL.

### note.attachments
Retrieves a list of attachments present in the note.

### note.backlinkContents
Retrieves content from backlinks referencing the note from a specific source note.

### note.backlinks
Gets an iterable list of notes linking to the current note.

### note.content
"Get the content of the note, as markdown."

### note.delete
Removes the note entirely.

### note.images
"Get all inline images in the note."

### note.insertContent
"Inserts content at the beginning of a note."

### note.insertTask
Inserts a new task at the note's beginning, returning the task UUID.

### note.name
Retrieves the note's title.

### note.publicURL
Returns a link to the published version if the note is published.

### note.publish
"Publish the note" and receive its public URL.

### note.removeTag
Removes a tag from the note.

### note.replaceContent
"Replaces the content of the entire note, or a section of the note, with new content."

### note.sections
"Gets the sections in the note."

### note.setName
Updates the note's title.

### note.tags
"Returns an Array of tags that are applied to the note."

### note.tasks
"Gets the tasks in the note."

### note.updateImage
Updates specific image properties (such as captions).

### note.url
"Returns the String URL of the note."
