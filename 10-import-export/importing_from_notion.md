# Importing from Notion

> [← Help Index](../00-index.md) · Category: [Import & Export](./index.md) · [Source ↗](https://www.amplenote.com/help/importing_from_notion)

This article describes the process of importing data from an existing Notion account.

Notion has a straightforward [documentation](https://www.notion.so/help/workspace-settings#export-an-entire-workspace) on exporting data from it, so following it should result in a smooth export experience, but there are some things you need to keep in mind:

- Your databases will not be imported
- Page layout and other non-markdown formatting will not be preserved
- Non-image attachments are not imported

We're constantly extending support for importing from other applications, so please email us at support@amplenote.com if you run into any issues/have suggestions for improving the importing process.

## Steps to import from Notion

To export your whole workspace:

1. Open "Settings & members"
2. Choose "Settings" under "Workspace"
3. Scroll down and choose "Export all workspace content"

![Exporting all workspace content in Notion](https://images.amplenote.com/ac237250-b212-11ed-9c4d-3ac2ea44f0fb/1c70c833-c4f6-42a7-a7f5-60069ec96744.png)

*[Screenshot showing the export workspace content option]*

To export a single page:

1. Open the page you want to export
2. Click on the three dots on the top right side
3. Choose "Export"

In the export menu you will need to change the Export Format to "CSV and Markdown" for you to be able to import your pages into Amplenote.

![Changing the export format to "CSV and Markdown"](https://images.amplenote.com/ac237250-b212-11ed-9c4d-3ac2ea44f0fb/30d3101e-a953-4f0d-919d-9f504fb05ce2.png)

*[Screenshot showing the export format selection menu]*

This will result in a .zip file being downloaded, where:

- Pages without databases will be exported as Markdown files
- Pages with databases will be exported as CSV files

To import these files into Amplenote, go to [the import and export page in your account](https://www.amplenote.com/account/import_export) and choose the option "Import Markdown", choose your .zip file and click on "Start import". When the import is complete you will be notified via email.
