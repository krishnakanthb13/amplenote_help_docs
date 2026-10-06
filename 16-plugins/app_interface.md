# App interface: Plugin methods to interact with user notes

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins/app_interface)

## Overview

The app interface provides methods for interacting with Amplenote. It's passed as the first argument to all plugin action functions and returns Promises.

**Markdown Version:** Available at https://public.amplenote.com/C8TUXf394zsvrGn8NwXgoJ7f.md

---

## Core Methods

### app.addNoteTag
Adds a tag to a note.

**Arguments:** `noteHandle`, tag string
**Returns:** Boolean indicating success
**Throws:** If tag argument is not a string

### app.addShortcut
Adds shortcuts to sidebar areas (calendar, jots, notes, tasks).

**Arguments:** Area string, shortcut object with filter properties
**Returns:** True once added
**Throws:** If invalid area or missing filter properties

### app.addTaskDomainNote
Ensures a note is included in a task domain.

**Arguments:** Task domain UUID, `noteHandle`
**Returns:** Boolean indicating success

### app.alert
Displays a message dialog with optional action buttons.

**Arguments:** Message string, optional options object
**Returns:** Action index, value, null, or -1
**Supports:** Custom icons, primary actions, scrolling

![Example showing preface text displayed before main message](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/53d98444-82b5-46c4-888a-ac47da8bfa74.png)

![Alert dialog example](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/1facb8f0-33ae-4abc-98d3-9b3aae94d44c.png)

![Alert with action button example](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/2a4d7d14-a28d-4051-a444-f26725038f15.png)

### app.attachNoteMedia
Uploads media files and associates them with notes.

**Arguments:** `noteHandle`, data URL
**Returns:** URL of uploaded media
**Throws:** If file too large or network errors occur

### app.callPlugin
Calls another plugin's `onPluginCall` function.

**Arguments:** Target plugin object, additional args
**Returns:** Result from called plugin or undefined

### app.context
Provides invocation location details and interaction methods.

**Properties:**
- `checkForUpdates` — Check if plugin is out of date
- `closeEmbed` — Closes open sidebar or modal embed
- `embedArgs` — Arguments for `onEmbedCall`
- `getStyleProperties` — Returns host client CSS styling and theme properties
- `lightDarkMode` — Current theme ("light" or "dark")
- `link` — Link properties if invoked from link
- `noteUUID` — UUID of current note
- `pluginUUID` — UUID of plugin note
- `refreshNotesList` — Requests host client to refresh displayed notes list
- `refreshSettings` — Reloads plugin settings
- `renderEmbed` — Re-renders embed
- `renderEmbedTarget` — Where embed is rendering
- `replaceSelection` — Replaces selected markdown
- `selectionContent` — Current selection markdown
- `setEmbedHTML` — Updates active embed HTML content dynamically
- `setScheduledTasks` — Progressively displays suggested scheduled tasks during `suggestScheduledTasks`
- `setStatus` — Displays a status message in the client UI
- `setTaskTargetNotes` — Progressively displays suggested note targets during `suggestTaskTargetNotes`
- `subscriptionLevel` — User tier (personal/pro/unlimited/founder)
- `taskUUID` — Task UUID if in task
- `updateEmbedArgs` — Updates embed arguments
- `updateImage` — Updates image properties
- `updateLink` — Updates link properties
- `url` — Current app location URL

### app.createNote
Creates a new note with optional name and tags.

**Arguments:** Name string, tags array, options object
**Returns:** UUID of new note

### app.deleteNote
Deletes a note (restorable for 30 days).

**Arguments:** `noteHandle`
**Returns:** Boolean indicating note existence

### app.evaluateExpression
Evaluates editor expression strings.

**Arguments:** Expression string
**Returns:** Result or null if invalid

### app.filterNotes
Finds notes matching filter criteria.

**Arguments:** Filter object with tag/query/group/taskDomainUUID, optional sort order
**Returns:** Array of matching `noteHandle`s
**Sort Options:** "changed", "created", "opened", "relevance", "title", "updated"

### app.findNote
Retrieves a `noteHandle` with metadata.

**Arguments:** `noteHandle` with uuid or name (and optional tags)
**Returns:** `noteHandle` with details or null

### app.getAttachmentURL
Gets temporary URL for an attachment.

**Arguments:** Attachment UUID
**Returns:** Temporary access URL

### app.getCompletedTasks
Gets tasks completed in a time range.

**Arguments:** Unix timestamps (from, to), optional options with taskDomainUUID
**Returns:** Array of completed task objects

### app.getExternalCalendarEvents
Retrieves cached external calendar events (next ~30 days).

**Arguments:** Optional options with days (1–30) and taskDomainUUID
**Returns:** Array of external calendar event objects

### app.getMoodRatings
Retrieves mood ratings within a time range.

**Arguments:** Unix timestamps (from, optional to)
**Returns:** Array of mood rating objects

### app.getNoteAttachments
Lists attachments currently referenced in a note.

**Arguments:** `noteHandle`
**Returns:** Array of attachment objects or null

### app.getNoteBacklinkContents
Gets content of backlinks with context.

**Arguments:** Target `noteHandle`, source `noteHandle`
**Returns:** Array of markdown strings

### app.getNoteBacklinks
Lists notes linking to specified note.

**Arguments:** `noteHandle`
**Returns:** Array of referencing `noteHandle`s

### app.getNoteContent
Retrieves note markdown content.

**Arguments:** `noteHandle`
**Returns:** Note content as markdown

### app.getNoteImages
Gets inline images in a note.

**Arguments:** `noteHandle`
**Returns:** Array of image objects

### app.getNoteOpenCounts
Returns note open statistics.

**Arguments:** `noteHandle`
**Returns:** Object with week/month/quarter counts or null

### app.getNotePublicURL
Gets public URL if note is published.

**Arguments:** `noteHandle`
**Returns:** Public URL or null
**Throws:** If network request fails

### app.getNoteSections
Lists sections delimited by headings or rules.

**Arguments:** `noteHandle`
**Returns:** Array of section objects

### app.getNoteSettings
Gets note-specific styling settings.

**Arguments:** `noteHandle`
**Returns:** Object with backgroundColor, bannerImageURL, maxOpenTasks or null

### app.getNoteTasks
Returns tasks in a note.

**Arguments:** `noteHandle`, optional options with includeDone boolean
**Returns:** Array of task objects

### app.getNoteURL
Gets full Amplenote URL for a note.

**Arguments:** `noteHandle`
**Returns:** Note URL string

### app.getPeople
Lists people known to the current user.

**Arguments:** None
**Returns:** Array of `person` objects

### app.getPreviousTaskInstances
Gets previous instances of a repeating task, newest first (given task itself not included). Async iterable recommended.

**Arguments:** Task UUID string
**Returns:** Array / Async Iterable of `task` objects

### app.getShortcuts
Lists shortcuts in an area.

**Arguments:** Area string (calendar/jots/notes/tasks)
**Returns:** Array of shortcut objects

### app.getTags
Retrieves all tags in account.

**Arguments:** None
**Returns:** Array of tag objects

### app.getTask
Gets details of a single task.

**Arguments:** Task UUID
**Returns:** Task object or null

### app.getTaskDomains
Gets list of task domains.

**Arguments:** None
**Returns:** Array of task domain objects with name, notes, uuid

### app.getTaskDomainTasks
Gets tasks in a task domain (supports async iteration).

**Arguments:** Task domain UUID
**Returns:** Array of task objects

### app.htmlFromContent
Converts markdown to HTML.

**Arguments:** Markdown content string
**Returns:** HTML string wrapped in ample-editor container
**Throws:** If content not a string

### app.insertNoteContent
Inserts content into a note.

**Arguments:** `noteHandle`, markdown string, optional options with atEnd boolean
**Throws:** If content exceeds 100k characters or note is readonly

### app.insertTask
Inserts new task at note beginning.

**Arguments:** `noteHandle`, task object with content/hideUntil/startAt
**Returns:** New task UUID
**Throws:** If content invalid for task or note locked

### app.navigate
Opens app to specified Amplenote URL.

**Arguments:** Amplenote URL string
**Returns:** Boolean indicating success

**Supported URLs:**
- Jots area: `https://www.amplenote.com/notes/jots`
- Notes filtered by tag: `https://www.amplenote.com/notes?tag=some-tag`
- Specific note: `https://www.amplenote.com/notes/NOTE_UUID`
- Note section: `https://www.amplenote.com/notes/NOTE_UUID#Section_name`
- Specific task: `https://www.amplenote.com/notes/tasks/TASK_UUID`

### app.notes
Alternative interface for note interactions.

**Methods:**
- `create(name, tags)` — Creates note, returns Note interface
- `dailyJot(timestamp)` — Gets daily jot, returns Note interface
- `filter(criteria)` — Filters notes, returns array of `noteHandle`s
- `find(uuid or noteHandle)` — Gets Note interface or null

### app.openEmbed
Adds plugin section to sidebar for full-screen embed.

**Arguments:** Optional arguments passed to renderEmbed
**Returns:** Nothing

![Plugin section in sidebar](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/e113eca3-1df8-4771-8f55-bd7e5b07b633.png)

### app.openSidebarEmbed
Opens embed in Peek Viewer sidebar.

**Arguments:** Aspect ratio (number/object), additional args
**Returns:** Boolean indicating success

![Quick open invocation example](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/4fc7ac45-540a-4a80-b7bc-8499dfcc78eb.png)

![Peek Viewer sidebar rendering](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/4f53f093-f4df-44a2-a5cc-8f43863309ce.png)

### app.prompt
Shows message with input fields.

**Arguments:** Message string, optional options object
**Returns:** User input value(s) or null

**Input Types:** checkbox, date, note, radio, secureText, select, string, tags, text
**Options:** inputs array, actions array, primaryAction object

![Basic prompt example](https://images.amplenote.com/2ae961e0-bc5d-11ed-808b-e21efa2d8566/13b30929-c82f-48e1-86e1-8d4642b59e3b.png)

![Multi-input prompt dialog](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/be4385e1-2902-4fc9-a8d9-43ddff8f1dea.png)

![Extended prompt with multiple input fields](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/f12cae67-340a-4886-90b5-af10d1b06a12.png)

![Prompt with action buttons](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/9d1fba7c-a047-403e-b7d9-e60f579ca917.png)

### app.publishNote
Publishes a note.

**Arguments:** `noteHandle` (must be remote)
**Returns:** Public URL or null
**Requirements:** Unlimited/Founder subscription, internet connection

### app.recordMoodRating
Records a mood rating.

**Arguments:** Rating integer (-2 to +2)
**Returns:** Rating UUID string

### app.removeNoteTag
Removes a tag from a note.

**Arguments:** `noteHandle`, tag string
**Returns:** Boolean indicating success
**Throws:** If tag argument not a string

### app.removeShortcut
Removes a shortcut from an area.

**Arguments:** Area string, shortcut object
**Returns:** True always

### app.replaceNoteContent
Replaces entire note content or section content.

**Arguments:** `noteHandle`, markdown string, optional options with section/includeCompletedTasks/includeHiddenTasks
**Returns:** Boolean indicating success
**Throws:** If content exceeds 100k characters or note readonly

### app.saveFile
Saves a file locally.

**Arguments:** Blob/File object, filename string
**Returns:** Promise resolving when save requested

### app.searchNotes
Full-text searches note content.

**Arguments:** Query string
**Returns:** Array of matching `noteHandle`s (best matches first)

### app.setNoteName
Sets a new note name.

**Arguments:** `noteHandle`, new name string
**Returns:** Boolean indicating success
**Throws:** If name not a string

### app.setNoteSetting
Sets note-specific settings.

**Arguments:** `noteHandle`, setting key, value
**Supported Keys:** backgroundColor (hex string), maxOpenTasks (integer)
**Returns:** Boolean indicating success

### app.setSetting
Updates user plugin settings.

**Arguments:** Setting name, new value string
**Returns:** Nothing

### app.settings
Object containing user-configured plugin settings (all strings).

### app.unpublishNote
Unpublishes a note.

**Arguments:** `noteHandle`
**Returns:** Boolean indicating not-published status
**Throws:** If network unavailable

### app.updateMoodRating
Updates mood rating properties.

**Arguments:** Rating UUID, updates object (note/rating)
**Returns:** Nothing
**Throws:** If UUID missing or invalid properties

### app.updateNoteImage
Updates image in a note.

**Arguments:** `noteHandle`, image object, updates object
**Returns:** Boolean indicating success
**Throws:** If markdown invalid in caption

### app.updateTask
Updates task properties or content.

**Arguments:** Task UUID, updates object
**Returns:** Boolean indicating success

### app.writeClipboardData
Writes to clipboard with cross-platform support.

**Arguments:** Data string, optional MIME type
**MIME Types:** text/plain, image/png (base64 encoded)
**Returns:** Nothing
**Throws:** If unsupported MIME type or invalid encoding

---

## Code Examples

**Adding a tag:**
```javascript
const added = await app.addNoteTag({ uuid: noteUUID }, "some-tag");
await app.alert(added ? "Tag added" : "Failed to add tag");
```

**Filtering notes:**
```javascript
const noteHandles = await app.filterNotes({ tag: "daily-jots" });
return `note count: ${noteHandles.length}`;
```

**Displaying alerts with actions:**
```javascript
const actionIndex = await app.alert("This is an alert", {
  actions: [{ icon: "post_add", label: "Insert in note" }]
});
```

**Getting note content:**
```javascript
const markdown = await app.getNoteContent({ uuid: noteUUID });
app.alert(markdown);
```

**Creating notes:**
```javascript
const uuid = await app.createNote("some new note", ["some-tag"]);
app.alert(uuid);
```

**Inserting content:**
```javascript
await app.insertNoteContent({ uuid: noteUUID }, "this is some **bold** text");
```

**Prompting user input:**
```javascript
let result = await app.prompt("Enter text");
return result;
```

**Using Note interface:**
```javascript
const note = await app.notes.create("new note", ["tag"]);
app.alert(note.uuid);
```

---

## Related Resources

- [Developing Amplenote Plugins Guide](https://www.amplenote.com/help/guide_to_developing_amplenote_plugins)
- [Note Interface](./note_interface.md)
- [Plugin Actions](./actions.md)
- [Data Types Appendix](./appendix_i.md)
