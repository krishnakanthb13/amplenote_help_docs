# Importing from Roam

> [← Help Index](../00-index.md) · Category: [Import & Export](./index.md) · [Source ↗](https://www.amplenote.com/help/import_from_roam)

## How do I import from Roam?

**The first step is to export your existing Roam data:**

To import from Roam, export your data by selecting "Export All" and the JSON Export Format. Expand the zip file to get a single .json file containing your exported data.

**Once you've exported your Roam data:**

1. Click the Amplenote Settings gear icon in the lower-left corner of the application to view your account settings
2. Select the "Import Notes" tab
3. Click the button to "Import from Roam"
4. Click the "Start import" button

![Screenshot showing the import interface with a start button](https://images.amplenote.com/e9b777b6-290b-11eb-b8b3-82d05cdc73d2/31f7b118-16db-4f65-b88a-2392afcc225c.png)

💡 Notes imported from Roam will be automatically tagged with `imported/roam`.

## What is imported?

- Any note references `[[Link to a note]]`
- Any inline tags `#Inline tag` - Inline tags are imported as note references; the reference will spell "#Inline tag", while the note itself will be titled "Inline tag", without the pound `#` sign. Note that in Amplenote, "tags" are a different abstraction. [Learn more here](/help/tag_shortcuts_default_shortcut#Tag_Shortcuts%2C_and_the_Default_Shortcut)
- Any image attachments

## What limitations exist for Roam imports?

While we strive to import your Roam notes in their entirety, there are some features not currently supported. Contact [support@amplenote.com](mailto:support@amplenote.com) if any are deal-breakers.

- Tables, boards, sliders, and diagrams are not imported
- `attributes::` are imported as plain text
- `{{[[DONE]]}}` blocks import with a check-mark icon, not an Amplenote task (`{{[[TODO]]}}` blocks do import as Amplenote tasks)
- Encrypted blocks are imported—including the hint—but do not include UI to decrypt the block

## How many notes can I import?

There is no limit to the number of notes you can import from Roam. Many Amplenote users have 5,000+ notes.

## How long does importing take?

It can take anywhere from 10 minutes to a few hours for the import to complete, depending on the size of the file being imported.

## Do I need to leave Amplenote open while my Roam data is importing?

Nope! The importer will continue to run if you close the site or application.

## What are Amplenote's storage limits?

There are no specific limits for how much data can be imported from Roam. Overall storage limits for Amplenote vary depending on the plan subscribed to:

- Basic - 10GB
- Pro - 25GB
- Founder - 25GB
