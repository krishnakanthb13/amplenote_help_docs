# Using Local Backups With External Tools and AI Workflows

> [← Help Index](../00-index.md) · Category: [Extending Amplenote](./index.md) · [Source ↗](https://www.amplenote.com/help/local_backups_with_ai_llm_tooling)

## How local backup sync works

Amplenote Desktop maintains local backup copies of notes for offline access and external workflows. When you modify a note in Amplenote, changes are written to both local backup files and synced to servers when connected. Notes are saved as Markdown (`.md`) files with internal identifiers for backup continuity.

**Important limitation:** "Renaming backup files or moving them from their original locations can break continuity with future backups." Local backups function as one-way exports—changes to local files don't sync back into the app and may be overwritten by future updates.

## Using external tools with local backups

You can interact with locally saved notes using various external tools, including:

- Saving notes as external archives
- Accessing them via file lookup apps like RayCast or Ulauncher
- Reading files with alternative text editors
- Searching contents using terminal commands or indexing tools
- Using AI agents to analyze, summarize, or transform backup files

These workflows suit experimentation, offline analysis, and temporary projects.

## Using AI tools with local backups

AI tools accessing device files can read and modify Markdown backups. However, "changes made by these tools to local backup files are not synced back into Amplenote and may be overwritten the next time the original note is updated."

Local backups work best for experimentation, analysis, temporary workflows, or providing context to external tools rather than as primary editing workflows. This preserves Amplenote as the authoritative source.

## Common misconceptions

**Edits to local files won't update in Amplenote.** Changes made locally aren't imported back.

**Local edits can be overwritten** by future note updates from Amplenote.

**Renaming backup files** may cause Amplenote to generate new backup files instead of updating renamed ones.

**Privacy with external AI tools** depends on your preferences and the third-party tool's data handling practices.

## When to use external AI tools vs Ample Agent Pro

Ample Agent Pro is a paid Amplenote plugin enabling frontier AI model access within the app.

| Use Case | Local Backups + External Tools | Ample Agent Pro |
|----------|-------------------------------|-----------------|
| Offline/local experimentation | Good fit | Less relevant |
| Persistent note editing | Not recommended | Better fit |
| Safe in-app workflows | Limited | Designed for this |
| Automatic integration | No | Yes |
| Controlled experience | No | Yes |
| Risk of unintended AI modifications | Lower | Depends on workflow |

## Best practices

- Treat local backups as exports or backup copies, not bidirectional sync
- Keep Amplenote as your primary editing location
- Avoid relying on local file edits as permanent changes
- Exercise caution sharing notes with third-party AI tools
- Test experimental workflows on non-critical notes first
