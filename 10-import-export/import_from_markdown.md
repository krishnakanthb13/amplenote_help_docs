# Import from Markdown

> [← Help Index](../00-index.md) · Category: [Import & Export](./index.md) · [Source ↗](https://www.amplenote.com/help/import_from_markdown)

Are you using Bear, Obsidian, or any other the numerous note taking apps that export to markdown?

Do you have one-off markdown files that you want to incorporate into your note taking system?

## Importing markdown zip files

Amplenote makes it easy to incorporate any markdown-flavored content, including cross-linked notes, images and formatting.

*[Screenshot showing Amplenote import interface — Settings > Import > Import Markdown button in upper right]*

From this page, you pick your markdown or zip file, click "Start import," and we'll show you a progress bar so you can decide whether to stick around and wait for the import, or whether to switch to another task.

## What Amplenote imports

As a general rule, we've tried to ensure that any concept that's in Obsidian can be imported into Amplenote. This includes:

- Images
- Cross-note links (aka "note references")
- Formatting (bold, italic, strikethrough)
- Headers
- External links
- Quotations
- Code blocks
- Inline literals
- ...and more

If there is a specific feature you'd like us to add to our importer, please vote for or create it at [our Feature Voting board](https://amplenote.com/feature_vote).

## Import from SQLite, Mysql, and other databases via Markdown (Import from Things)

You can create a markdown file to import from using SQL like the following:

```
# If you're in a database like Mysql that supports this syntax, consider uncommenting this:
# SET NAMES utf8;

SELECT tasks_field
INTO OUTFILE '/path/to/amplenote_import_data.md'
OPTIONALLY ENCLOSED BY '"'
LINES TERMINATED BY '\n[]'
FROM your_table
```

[See this StackOverflow post for more tips on outputting a SQL table to a file](https://stackoverflow.com/questions/1119312/mysql-export-into-outfile-csv-escaping-chars).

## Our commitment to help you avoid data lock-in

We want to ensure it's as straightforward as possible to jump between Amplenote and other note taking apps. Read more at our [Exporting Your Notes](/help/export_your_notes) page.

## Importing from individual markdown files

There are a couple options ways to bring a markdown file into Amplenote.

Option one is to drop your markdown note file into the notes list (when Notes View is open, and you have at least two panes visible, notes list will be to left of the main note body). When you drop a note into the notes list, it becomes a new note, with all the content from your markdown file interpreted.

Option two is to drop the file into an existing note body. In this case, we will treat the markdown file as an attachment, which can be opened and viewed.

## Metadata from imported markdown files

Below is a known list of options that can be set in the frontmatter section of a markdown file that Amplenote will interpret and import accordingly:

- `title`
- `created`
- `tags`

Example: if you import a markdown file like the following:

```
---
title: 'December 13th, 2024'
created: '2024-12-13T08:36:52-08:00'
tags:
- daily-jots
---

This is a note and here are its contents
```

The resulting note in Amplenote will have:

- The title `December 13th, 2024` (instead of the default title, which is the name of the markdown file on your disk)
- The "created date" set to December 13, 2024
- And the tag list set to `daily-jots`
