# Calendar Task Domains

> [← Help Index](../00-index.md) · Category: [Calendars & Scheduling](./index.md) · [Source ↗](https://www.amplenote.com/help/using_calendar_task_domains)

## Overview

Task Domains are collections of notes and tags that Amplenote extracts to-do items from to populate the task list displayed alongside the calendar. Without configuring a Task Domain, tasks won't appear next to the calendar.

The platform offers three default Task Domains: "Work," "Personal," and "Misc." Each can be renamed or hidden. Tasks scheduled from a Task Domain can be drag-and-dropped onto the Amplenote calendar and automatically synchronized to external Google or Outlook calendars.

## Why Care About Task Domains?

Task Domains allow users to specify all notes and tags containing tasks within a particular life realm. A broad Task Domain like "Work" may encompass numerous disparate projects — some old, some new, some still relevant, others not.

As of 2021, Amplenote permits configuration of up to three separate Task Domains.

![Each of the colored boxes represents one Task Domain you can configure](https://images.amplenote.com/e0b7ce82-60eb-11eb-bad5-2a844617cbef/31195eb5-0581-48a2-85ab-71639eaa1784.png)

### Adding Content to Task Domains

**Notes:** When adding a note, its tasks become eligible to appear in the Calendar Sidebar Task List when that Task Domain is selected. If a task has a Start Time set, it syncs to specified external calendars and disappears from the sidebar task list.

**Tags:** Adding a tag to a Task Domain scans all notes containing that tag for tasks. For example, adding the tag `todo/marketing` includes all notes tagged with that label (including hierarchical subtags like `todo/marketing/client-a`) in the task list.

## Locating Task Domains

Task Domains are found in Account Settings under "Task Calendar," or accessible directly via the Task Calendar settings link.

![Navigating to Task Calendar under Amplenote account settings](https://images.amplenote.com/e0b7ce82-60eb-11eb-bad5-2a844617cbef/270cf770-8a80-49ff-8aab-454d11d78e75.png)

## Task Domain Options

Each Task Domain includes several configuration options:

![Normal and advanced options to configure a Task Domain](https://images.amplenote.com/e0b7ce82-60eb-11eb-bad5-2a844617cbef/84c1dd59-e96f-486c-8cbc-63519dfbe939.png)

### Renaming Task Domain

A pencil icon next to each Task Domain's name allows renaming, with a 10-character limit for mobile calendar compatibility.

### Notes

Specifies which notes' tasks display when the Task Domain is selected. Archived notes or those without tasks don't appear.

### Tags

Determines which tagged notes contribute tasks. Adding a parent tag includes all hierarchical subtags automatically.

### Calendar Sync

Controls which external calendars display events and receive published tasks. Options include "Show events only" or "Show events and publish tasks" (the latter requires Pro subscription or higher). Task details sync as private events to external calendars, with Rich Footnotes included in event descriptions.

![Calendars can be connected as input sources or with full two-way sync](https://images.amplenote.com/e0b7ce82-60eb-11eb-bad5-2a844617cbef/3d09af9b-e90e-44a3-81bc-ba2f6e3dedf5.png)

### Default Duration & Default Reminder

**Default Duration:** Sets initial time allocation when creating new calendar events or dragging unscheduled tasks onto the calendar. Can be adjusted by dragging task edges.

**Default Reminder:** For standalone Amplenote calendar use, enables notifications for newly created tasks. For calendar-synced setups, external calendars handle notifications.

![Default duration and default reminder settings for a Task Domain](https://images.amplenote.com/e0b7ce82-60eb-11eb-bad5-2a844617cbef/6a8188ea-6f1a-4f73-93e8-2df058291430.png)

### Suppress Reminders for Imported Events

Prevents notifications for events imported from synchronized calendars; unchecking allows reminders for imported events.

### Hide Task Domain

Removes a Task Domain from calendar display without deletion.

### First Day of Week

Applies globally across all Task Domains (not domain-specific).

### Completed Events on External Calendar

Controls whether completed tasks propagate to synced external calendars.

![Setting controlling whether completed events show on the external calendar](https://images.amplenote.com/e0b7ce82-60eb-11eb-bad5-2a844617cbef/2d07f465-663d-4c2f-a095-62fbab25260d.png)

## Frequently Asked Questions

### Why Do Scheduled Events Appear Gray?

Tasks scheduled without expected colors typically aren't included in the currently viewed Task Domain. The Calendar Coloring help page explains various workarounds.

### Why Can't I Include Every Task Everywhere?

Limiting calendar inclusion by Task Domain tags prevents unwanted behavior: shared notes' scheduled tasks wouldn't clutter the calendar; temporary planning notes wouldn't populate calendars; imported notes from other apps wouldn't overwhelm calendars with outdated tasks. This design allows easy toggling between "work" and "weekend" task views.

### Can Notes Be Automatically Tagged for Calendar Inclusion?

Yes. Using the note reference syntax `@&` automatically applies the current note's tags to newly created or linked notes, as described in the note linking help documentation.

## Additional Resources

A four-minute video tutorial on YouTube provides a visual walkthrough of this content.

![Using Calendar Task Domains video tutorial](https://images.amplenote.com/e0b7ce82-60eb-11eb-bad5-2a844617cbef/61175b10-5fab-432e-b45f-79d52761d88c.png)
