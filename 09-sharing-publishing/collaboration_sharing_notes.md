# Shared notes and shared tags

> [← Help Index](../00-index.md) · Category: [Sharing & Publishing](./index.md) · [Source ↗](https://www.amplenote.com/help/collaboration_sharing_notes)

Full title: "Shared notes and shared tags: flexible collaboration options"

## Overview

Amplenote provides three primary sharing methods: individual note sharing, shared tags for groups, and public web publishing.

## Sharing methods

### Individual notes

- Use the `/invite` or `/add` slash commands within notes.
- Click "Add Collaborators" from the note's triple-dot menu.
- Grant either edit or read-only access.
- Adjust permissions anytime via the share icon.

### Shared tags

The platform allows sharing entire tag-based note collections with collaborator groups. As described: "if they apply the shared tag, the note will be available for viewing, editing (if that permission was granted) and publishing."

**Implementation steps:**

1. Hover over the tag's triple-dot → select "Share tag."
2. Choose collaborators and permission levels.
3. Recipients view the shared tag at the `shared/[tag name]` path.
4. All subsequently tagged notes sync across collaborators.

## Important considerations

Shared tags function as controlled by the original sharer's account. The guidance advises: "it's best to have the original tag sharer be an account expected to exist in perpetuity, like support@yourcompany.com."

Notes created by collaborators become controlled by the tag sharer's account, though removing the tag simply revokes individual access rather than deletion.

Deleted shared notes remain visible to recipients unless explicitly removed beforehand.
