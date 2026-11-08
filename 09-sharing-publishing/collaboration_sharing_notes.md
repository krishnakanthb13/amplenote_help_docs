# Shared notes and shared tags

> [← Help Index](../00-index.md) · Category: [Sharing & Publishing](./index.md) · [Source ↗](https://www.amplenote.com/help/collaboration_sharing_notes)

Full title: "Shared notes and shared tags: flexible collaboration options"

## Overview

Amplenote provides three primary sharing methods: individual note sharing, shared tags for groups, and public web publishing.

## Sharing methods

### Individual notes

- Use the `/invite` or `/add` slash commands within notes.
- Click "Add Collaborators" from the note's triple-dot menu.
- Grant either edit or read-only access. An active "Edit" toggle grants edit access; only "Share" active means read-only.
- Adjust permissions anytime via the share icon.
- Use "Include a message" to send a message in the collaborator's notification email.
- Enable "Also share referenced notes" to grant recipients access to every note referenced inside the shared note. This does not recursively search for unshared notes within the linked notes; link all notes from the original note or share a note tag instead.

![Using Slash Menu to add new contributors](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/965e9693-d3c3-4de1-a190-0989f10972a7.png)

![Getting ready to add collaborators](https://images.amplenote.com/2f9dba8e-03e7-11e9-8493-fed38e33333f/b0238f4e-f3e9-456d-847c-2b13897f8c23.png)

![Collaborator dialog: showing frequent collaborators](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/3d696863-c812-4014-bd1b-c942c2f3ad25.png)

![Share icon shows how many have access, and re-opens collaboration dialog](https://images.amplenote.com/2f9dba8e-03e7-11e9-8493-fed38e33333f/89f65382-73cc-42ba-a22f-337ff59688aa.png)

![Controlling access granted to a user who currently has access](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/c39d5b16-347b-4275-9626-190589f1bbd2.png)

![Sending a message with the collaborator invitation](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/1bd47f0f-369f-4a1d-b779-2458041ffc3f.png)

![The warning that recipient notes become controlled by the sharer](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/17ad52a2-b3b4-4650-8a4e-c0a51320992d.jpg)

![View all details](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/5fc290a2-5a7b-4212-b8f4-15d40ec11bbd.jpg)

### Sharing all notes linked to by a note

![Sharing all notes linked to by a note](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/58598afe-3685-45ed-95b2-f77e6fe016d0.png)

### Viewing notes recently updated by a collaborator

![Viewing notes recently updated by a collaborator](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/52692dcf-48ba-4145-b8ff-b87eb8dee75c.png)

### Shared tags

The platform allows sharing entire tag-based note collections with collaborator groups. As described: "if they apply the shared tag, the note will be available for viewing, editing (if that permission was granted) and publishing."

**Implementation steps:**

1. Hover over the tag's triple-dot → select "Share tag."
2. Choose collaborators and permission levels.
3. Recipients view the shared tag at the `shared/[tag name]` path.
4. All subsequently tagged notes sync across collaborators.

![Hovering on a tag's triple dot and choosing "Share tag"](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/8e1345dd-a546-44b8-aa1a-04c80fd88a2d.jpg)

![Choosing who to share the notes in the tag with](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/372a1a0b-854a-4727-a5f4-092a440efba6.jpg)

![The Amplenote account that received the tag share will often want to rename it](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/97147dd5-e7d2-4597-9566-45820dc6d610.jpg)

## Important considerations

Shared tags function as controlled by the original sharer's account. The guidance advises: "it's best to have the original tag sharer be an account expected to exist in perpetuity, like support@yourcompany.com."

Notes created by collaborators become controlled by the tag sharer's account, though removing the tag simply revokes individual access rather than deletion.

Deleted shared notes remain visible to recipients unless explicitly removed beforehand.

## Tracking shared notes

As of early 2026, new users get a **Mission Control Dashboard → "Shared Notes"** component, which tracks which shared notes have been updated since you last saw them. The default view shows recently-updated notes you haven't opened; a contributor dropdown (default `All contributors`) filters a paginated list, most-recently-updated first.

## Publishing a group of notes

Publishing a group of notes requires an **Unlimited or Founder subscription** with "Publish" enabled, using the **Webnotes plugin** (<https://www.amplenote.com/plugins/Mor4CfsPFGmF34LHkEo4MeaJ>).

## Inviting collaborators

Amplenote offers referral bonuses / swag for referred users who subscribe.

## Screenshots

![Viewing the note creator and sharer in the note details](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/94cb518e-b41b-4bfb-bc02-ed1142e1aa9a.jpg)

![Spotting a shared note in Notes View mode note list](https://images.amplenote.com/652dbac0-fad3-11ea-a5bc-f200a12bf340/343c2ef2-133f-4d84-a94b-78fcecf8d81d.png)
