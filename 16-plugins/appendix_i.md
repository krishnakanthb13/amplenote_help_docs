# Appendix I: Types

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins/appendix_i)

## Overview
This reference documentation catalogs the type definitions available in the Amplenote Plugin API.

## Type Definitions

### attachment
Describes file attachments within notes, containing:
- `name`: String filename
- `type`: MIME type string
- `uuid`: Unique string identifier

### externalCalendarEvent
Represents events from connected external calendars with properties:
- `allDay`: Boolean for all-day events
- `calendar`: Object with `color` (hex), `name`, `provider` ("google_calendar", "apple_calendar", "outlook_calendar", etc.), and `uuid`
- `color`: Hex color string for the event
- `end`: Date when event ends
- `start`: Date when event starts
- `title`: Event title string

### image
Describes inline images in notes:
- `caption`: Markdown string for image caption
- `index`: Disambiguates multiple images with same source
- `src`: Image source URL
- `text`: OCR-recognized text from image
- `width`: Optional pixel width for display

### link
Represents hyperlinks with optional Rich Footnote content:
- `description`: Markdown string for footnote content (subset of note markdown)
- `href`: Target URL string
- Properties may be `null` if not set

### moodRating
User-submitted mood ratings containing:
- `note`: User-entered string
- `rating`: Integer from -2 to +2
- `timestamp`: Unix timestamp in seconds
- `uuid`: Unique identifier string

### noteHandle
Objects identifying notes, including non-existent future notes. Can accept string `uuid` as shorthand. Returns populated with metadata:
- `changed`: ISO 8601 datetime of last user modification
- `created`: ISO 8601 creation datetime
- `name`: Note title string (null for untitled notes)
- `published`: Boolean (present only if true)
- `shared`: Boolean (present only if true)
- `tags`: Array of tag strings
- `updated`: ISO 8601 modification datetime
- `uuid`: Note identifier string
- `vault`: Boolean (present only if true)

### section
Represents note chunks divided by headings and horizontal rules:
- `heading`: Null or object with `anchor`, `href`, `level` (integer), and `text`
- `index`: Integer for distinguishing duplicate heading sections

### tag
User account tags containing:
- `color`: Hex color string without "#" prefix
- `noteCount`: Integer count of tagged notes
- `text`: Lowercase tag text with "/" delimiters

### task
Task objects with properties:
- `completedAt`: Unix timestamp if completed
- `content`: Markdown string describing task
- `createdAt`: Unix timestamp (immutable)
- `deadline`: Unix timestamp for task deadline
- `dismissedAt`: Unix timestamp if dismissed
- `endAt`: Unix timestamp for task end (must follow `startAt`)
- `hideUntil`: Unix timestamp or null
- `important`: Boolean flag
- `isParent`: Boolean for indented subtasks
- `isRepeating`: Boolean for repeating tasks
- `noteUUID`: Containing note identifier
- `repeat`: RRULE string or null
- `score`: Number representing task score
- `startAt`: Unix timestamp or null
- `urgent`: Boolean flag
- `uuid`: Task identifier string
