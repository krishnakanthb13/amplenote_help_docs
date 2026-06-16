# Importing from Todoist

> [← Help Index](../00-index.md) · Category: [Import & Export](./index.md) · [Source ↗](https://www.amplenote.com/help/importing_from_todoist)

## Overview

Amplenote offers a semi-automated method to import tasks from Todoist. However, task properties (aka start/due dates, flags, or labels) will not be preserved during this process.

## How to Import Todoist Tasks into Amplenote

### 1. Export Your Todoist Tasks

Follow Todoist's documentation to [create a backup of your projects](https://todoist.com/help/articles/introduction-to-backups-ywaJeQbN). This generates a zip file containing one CSV file per project.

### 2. Edit the Todoist CSV Export

Prepare the CSV files for import by:

- Opening each CSV file in Google Sheets or Microsoft Excel
- Removing all columns except "Content" and "Description"
- Deleting any empty lines in the spreadsheet

The edited spreadsheet should contain only these two columns with task data.

### 3. Import the Tasks into Amplenote

Complete the import process by:

- Copying the CONTENT and DESCRIPTION columns
- Pasting them into Amplenote as plain text
- Selecting all text and clicking the task button in the toolbar to convert lines into tasks
- Repeating these steps for every project

## Important Notes

Only task contents and descriptions transfer—other task properties or subtask relationships cannot be maintained. Todoist labels export as plain text and require manual conversion to note references if you wish to preserve them. Learn more about this feature in [Note Reference Filtering (aka "Inline Tags")](/help/inline_tags_note_reference_filtering).
