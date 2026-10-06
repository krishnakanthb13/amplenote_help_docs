# An overview: Importing notes and tasks from other apps

> [← Help Index](../00-index.md) · Category: [Import & Export](./index.md) · [Source ↗](https://www.amplenote.com/help/import_notes_and_tasks_overview)

Amplenote has built-in importers for the most common note and task apps, and can import any collection of notes formatted as markdown or JSON. For anything the built-in importers can't handle, desktop LLMs like Claude or Codex can read your export and write the data directly into Amplenote through its Model Context Protocol (MCP) server.

---

## What each importer brings across

The table below summarizes what comes across cleanly out of the box (✅), what isn't supported yet (❌), and what can be imported with a desktop LLM or manual effort (🛠️):

| Content type | Obsidian | Evernote | Todoist | Notion | Markdown zip | Roam |
|---|---|---|---|---|---|---|
| **Note text & formatting** | ✅ | ✅ | — | ✅ | ✅ | ✅ |
| **Images** | ✅ | ✅ | 🛠️ | ✅ | ✅ | 🛠️ |
| **Other attachments (PDF, Office docs)** | ✅ | ✅ | 🛠️ | 🛠️ | ✅ | 🛠️ |
| **Links between notes** | ✅ | ✅ | — | 🛠️ | ✅ | ✅ |
| **Tags, folders & notebooks** | ✅ | ✅ | 🛠️ | ✅ | ✅ | ✅ |
| **Tables** | ✅ | ✅ | — | ✅ | ✅ | 🛠️ |
| **Tasks (to-dos)** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Task dates, priorities & labels** | ✅ | ✅ | 🛠️ | 🛠️ | 🛠️ | 🛠️ |
| **Databases & structured properties** | ❌ | — | — | 🛠️ | — | 🛠️ |
| **Original "created" dates** | ✅ | ✅ | 🛠️ | ✅ | ✅ | ✅ |

---

## Import from Obsidian

![Obsidian import](https://images.amplenote.com/5936a114-bb5c-11f1-b98c-15337a027ee1/7df96c2a-c78b-4a80-9872-4f816714be72.png)

Obsidian is the most common starting point for new Amplenote users. Because Obsidian stores everything as standard markdown files, almost your entire vault comes across untouched: text, headings, formatting, images, links between notes, tags, code blocks, and attachments. The main gaps are community plugins (Dataview queries, Canvas boards, etc.), which don't map to Amplenote features.

**tl;dr:** Zip your vault folder, go to **Account Settings → Import & Export → Import Markdown**, choose the zip, and click **"Start import."** You'll get an email when it's done. Full instructions: [Import from Obsidian](./import_from_obsidian.md).

![Compressing an Obsidian vault](https://images.amplenote.com/3ba026fc-801d-11ee-89e6-e6e121a71ab4/cd3b73cb-b067-4768-991d-d061fdaf83f4.png)

---

## Import from Evernote

![Evernote import](https://images.amplenote.com/5936a114-bb5c-11f1-b98c-15337a027ee1/a545da28-92ac-4e9a-9071-31d58f0106ed.png)

Evernote has the most complete importer of any source. Notes, tags, formatting, indented lists, to-dos, images, tables, headings, and PDF/Word/Excel/PowerPoint attachments all come across from an `.enex` export, and there's no cap on how many notes you can bring (though very large imports can take a few hours, and keep running if you close Amplenote). Every imported note gets the tag `imported/evernote`. The main things lost are your notebook structure (notebooks don't become tags on their own), links between Evernote notes, and reminder dates. A determined user with a desktop LLM can map each notebook to its own tag, re-point internal note links, and turn reminders into scheduled tasks.

**tl;dr:** In Evernote, right-click a notebook and choose **Export notebook** (or select notes and use **Export**), save as `.enex`, and be sure to check **"Include tags for each note."** Then in Amplenote go to **Account Settings → Import & Export**, choose your `.enex` file, and click **"Start import."** Full instructions: [Importing from Evernote](./import_from_evernote_how_to.md).

![Choose your .enex file and click Start import](https://images.amplenote.com/99b5a684-03f6-11e9-9224-024f990c9f6a/7847d182-f21f-4696-9bd8-70f54be6ae19)

---

## Import from Todoist

![Todoist import](https://images.amplenote.com/5936a114-bb5c-11f1-b98c-15337a027ee1/31a913e0-fe87-464e-a4d0-74de3df29a94.png)

Todoist imports are semi-manual. With a few minutes per project, you can bring over every task's content and description by pasting them into a note and converting the lines to tasks. Everything else, including due dates, priorities, labels, subtask nesting, and comments, is lost with the easy method. If you're determined, this is the source where a desktop LLM pays off most: it can read the Todoist CSV backup (or the Todoist API) and recreate each task in Amplenote with its start date, turn labels into tags or note references, and put each project into its own note.

**tl;dr:** In Todoist, go to **Settings → Backups** and download a backup zip (one CSV file per project). Open each CSV in Google Sheets or Excel, delete every column except `Content` and `Description`, and copy what's left. Paste it into an Amplenote note as plain text, select all, and click the task button in the toolbar. Full instructions: [Importing from Todoist](./importing_from_todoist.md).

![A Todoist project CSV trimmed down to the Content and Description columns](https://images.amplenote.com/10a7518a-ade3-11ed-8eed-f27a94c8b4fd/39d84605-6c48-420a-89f6-4fbd2f4c83a0.png)

---

## Import from Notion

![Notion import](https://images.amplenote.com/5936a114-bb5c-11f1-b98c-15337a027ee1/3a31a95c-6748-4a81-9e2f-34ee80b7564d.png)

Notion's "Markdown & CSV" export brings your regular pages across easily: their text, headings, formatting, and images import through the markdown importer. Databases are the big gap. They're exported as CSV files, which the importer skips, and page layout (columns, embeds, toggles), non-image attachments, and database properties don't come across. If you're determined, a desktop LLM can turn each database CSV into an Amplenote table or a set of notes, turn database rows with checkboxes and dates into scheduled tasks, and re-link pages that referenced each other.

**tl;dr:** In Notion, open **Settings → General** (under Workspace) and choose **Export all workspace content**, or use the ••• menu on one page and choose **Export**. Set the export format to **"Markdown & CSV"** and download the zip. Then in Amplenote go to **Account Settings → Import & Export → Import Markdown**, choose the zip, and click **"Start import."** You'll get an email when it's done. Full instructions: [Importing from Notion](./importing_from_notion.md).

![Set Notion's export format to Markdown & CSV](https://images.amplenote.com/ac237250-b212-11ed-9c4d-3ac2ea44f0fb/30d3101e-a953-4f0d-919d-9f504fb05ce2.png)

---

## Import from a markdown zip file

![Markdown import](https://images.amplenote.com/5936a114-bb5c-11f1-b98c-15337a027ee1/09fc53f1-0f52-4dde-ba48-b06197562ac2.png)

Markdown is Amplenote's universal import format, so any app that exports markdown (Bear, Logseq, Joplin, Standard Notes, Google Keep after conversion, and more) can come across easily. A zip of `.md` files imports images (when they're in the zip), links between notes, formatting, headers, quotes, code blocks, and inline literals. Front-matter `title`, `created`, and `tags` fields are read too, so notes keep their original names, creation dates, and tags. Tables and task metadata are the main gaps. If you're determined, you can generate markdown from almost anything (even a SQLite or MySQL database, such as Things 3's) or have a desktop LLM add front matter and clean up your files before importing.

**tl;dr:** Export your notes as markdown from your current app, then compress the `.md` files (plus any images they reference) into one `.zip`. In Amplenote go to **Account Settings → Import & Export → Import Markdown**, choose the zip, and click **"Start import."** For a single file, just drag the `.md` file into your notes list. Full instructions: [Import from Markdown](./import_from_markdown.md). Coming from Google Keep? See [Importing from Google Keep](./import_from_google_keep.md).

![Settings → Import → Import Markdown](https://images.amplenote.com/559ee504-9387-11ec-8702-1a40fa241576/6963d904-c41e-48c1-a4d9-236bae03cb95.png)

---

## Import from Roam

![Roam import](https://images.amplenote.com/5936a114-bb5c-11f1-b98c-15337a027ee1/019a3244-4fbc-4e35-a84a-eed416ce8dc5.png)

Roam's JSON export brings over all of your pages with little effort, including `[[note references]]`, inline `#tags` (they become note references), images, and `{{[[TODO]]}}` blocks as real Amplenote tasks. There's no limit on note count, and many users have imported 5,000+ notes. Every imported note gets the tag `imported/roam`. What doesn't come across cleanly: tables, boards, sliders, and diagrams; `attributes::` (imported as plain text); `{{[[DONE]]}}` blocks (imported as a checkmark rather than a completed task); and encrypted blocks, which can't be decrypted in Amplenote. With a desktop LLM, you can rebuild tables, turn attributes into structured tables or tags, and convert DONE blocks into completed tasks.

**tl;dr:** In Roam, open the ••• menu (top right), choose **Export All**, pick the **JSON** format, and unzip the download to get one `.json` file. Then in Amplenote go to **Account Settings → Import & Export**, click **"Import from Roam,"** choose your file, and click **"Start import."** Full instructions: [Importing from Roam](./import_from_roam.md).

![Amplenote's Import from Roam screen](https://images.amplenote.com/e9b777b6-290b-11eb-b8b3-82d05cdc73d2/31f7b118-16db-4f65-b88a-2392afcc225c.png)

---

## Elaborate migrations with a desktop LLM

Every 🛠️ in the table above is something a desktop LLM like Claude or Codex can usually do for you. With Amplenote's MCP server turned on, the LLM can read your exported files on disk and write straight into your Amplenote account: it can create notes, insert tasks with start dates, apply tags, and attach images. That turns jobs that would take hours by hand into a single conversation, like rebuilding a Todoist backup with every due date intact, turning Notion database CSVs into tables, or mapping Evernote notebooks to tags.

**tl;dr:** Turn on MCP in **Amplenote Desktop → Settings** (Unlimited or Founder plans), copy the config for Claude Desktop, Claude Code, or Codex, and keep Amplenote Desktop open while the LLM works. Run the regular importer first for anything marked ✅, then give the LLM the export folder and describe what's missing. For example: *"Here's my Todoist backup folder. For each project, create an Amplenote note with the project's name, and add each task with its due date as the start date. Turn labels into tags."* Spot-check a few notes before letting it process everything. Setup instructions: [Claude & Codex: Enable MCP access to read and write notes on desktop](../15-extending-amplenote/ai_mcp_server_connect_amplenote_claude_codex.md).

If the importer doesn't cover something you need, drop by our Discord, or vote for it on the feature voting board. Founder subscribers can also email support for help with their import.
