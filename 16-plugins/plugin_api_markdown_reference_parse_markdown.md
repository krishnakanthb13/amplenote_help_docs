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

![Cycle colors index — light mode](https://images.amplenote.com/e4672d3e-3bee-11ef-8e0e-26e37c279344/080289cc-ea91-40fb-8614-9ff11bab8aef.png)

![Cycle colors index — dark mode](https://images.amplenote.com/e4672d3e-3bee-11ef-8e0e-26e37c279344/c7d12f6f-f05a-4e04-b913-53f60ad7729b.png)

## Rich Footnotes
Rich footnotes with images or descriptions append to note content using standard markdown footnote syntax:

```
[Rich Footnote][^1]
[^1]: [Description text]()
```

![Inserting a Rich Footnote](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/53eb85c9-e7d3-4a7f-92e3-b68fa595113c.png)

## Markdown Tables
Tables support complex formatting with custom syntax for enhanced cells. Column widths can be specified via HTML comments:

```
|name|Bullet Journal<!-- {"cell":{"colwidth":350}} -->|
```

![Inserting a markdown table](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/847c257f-1954-454f-8b78-41ce7e1b6927.png)

![Markdown table with column widths](https://images.amplenote.com/e4672d3e-3bee-11ef-8e0e-26e37c279344/8a14c4b1-3a0d-4860-96a7-c754b0b945a6.png)

## Line Breaks
Insert line breaks using backslashes between empty lines in template literals.

![Line breaks in markdown](https://images.amplenote.com/e4672d3e-3bee-11ef-8e0e-26e37c279344/c8cc9e43-88fa-43b4-a4a8-a3aa00e2422b.png)

## Collapsible Headings
Mark headings as collapsed using HTML comments:

```
# Heading 1 <!-- {"collapsed": true} -->
```

## Task Objects
Since September 2025, tasks can be created with markdown using HTML comments to assign UUIDs and properties like `completedAt` and `victoryValue`.

## JavaScript Expression
Use template literals for markdown blocks in JavaScript code.
