# Implement a "Table of Contents" sidebar on a published embedded note

> [← Help Index](../00-index.md) · Category: [Sharing & Publishing](./index.md) · [Source ↗](https://www.amplenote.com/help/publish_notes_with_table_of_contents_side_navigation)

This article provides a complete implementation guide for creating an auto-scrolling sidebar table of contents for Amplenote embedded content, as used by GitClear.

## Key components

### React component (`amplenote-sidebar-toc.js`)

The functional component manages highlighting sidebar links based on scroll position. It includes utilities for:

- Throttling scroll events using lodash to prevent performance degradation.
- Filtering out table-of-contents sections from the rendered list.
- Handling sticky parent positioning.
- Managing header depth indentation.

### Styling (`amplenote-sidebar-toc.scss`)

The SCSS provides responsive design across tablet, laptop, and desktop breakpoints, with features including:

- Sticky positioning for the sidebar.
- Collapsible functionality with an icon toggle.
- Hover and active states for links.
- Border styling for nested header depths.

### HTML structure

The sidebar must be implemented as a sibling to the Amplenote embed, wrapped in a parent container with flex layout to position the sidebar alongside the embedded content.

## Functional features

- Auto-scrolls the sidebar to keep the active section visible.
- Smooth scrolling behavior for link navigation.
- Responsive collapse functionality.
- Filters out nested "Table of Contents" sections.
- Requires a minimum of five sections to display.

The implementation listens to Amplenote embed events (`onAmpleEmbedTOC`, `onAmpleEmbedHeadingHighlight`) to synchronize content navigation.
