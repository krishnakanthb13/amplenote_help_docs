# Plugin Markdown Reference

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/plugin_api_markdown_reference_parse_markdown)

## Overview
Amplenote's Plugin API exchanges note content through markdown. Key methods include `app.getNoteContent`, `app.getNoteSections`, `app.insertTask`, `app.replaceNoteContent`, and `app.updateTask`. The syntax follows the "GitHub Flavored Markdown Spec."

## Markdown Basics
Users can download notes to view their markdown representation. Amplenote supports standard markdown formatting and allows developers to inspect markdown syntax by exporting formatted content.

## Colored Text and Colored Backgrounds
Color uses HTML comments within highlight elements (`==text==`). Color values are integers assigned to `cycleColor` or `backgroundCycleColor` keys:

```javascript
await noteInterface.insertContent(`==Red text<!-- {"cycleColor": "23"} -->==`);
```

Important: No spaces should appear between the opening `==` and text.

## Cycle Colors Index
Amplenote supports 60 colors with separate palettes for light and dark modes, automatically adapting colors based on theme selection.

## Rich Footnotes
Rich footnotes with images or descriptions append to note content using standard markdown footnote syntax:

```
[Rich Footnote][^1]
[^1]: [Description text]()
```

## Markdown Tables
Tables support complex formatting with custom syntax for enhanced cells. Column widths can be specified via HTML comments:

```
|name|Bullet Journal<!-- {"cell":{"colwidth":350}} -->|
```

## Line Breaks
Insert line breaks using backslashes between empty lines in template literals.

## Collapsible Headings
Mark headings as collapsed using HTML comments:

```
# Heading 1 <!-- {"collapsed": true} -->
```

## Task Objects
Since September 2025, tasks can be created with markdown using HTML comments to assign UUIDs and properties like `completedAt` and `victoryValue`.

## JavaScript Expression
Use template literals for markdown blocks in JavaScript code.
