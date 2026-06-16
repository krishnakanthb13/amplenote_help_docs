# Exporting your notes

> [← Help Index](../00-index.md) · Category: [Import & Export](./index.md) · [Source ↗](https://www.amplenote.com/help/export_your_notes)

We've all been burned by products that seemed promising, but where their potential was undone by hubris, apathy, or incompetence of the app developer. That's what makes it imperative for companies like ours to be transparent about the switching costs if you decide you want to leave Amplenote after having trusted it with your data.

So, where does "Note Exporting" fit among our relative development priorities? As you can read in this [blog post about Amplenote's core values](https://www.amplenote.com/blog/core_values_robust_export_fast_cancellation_always_listening), **robust exporting is the first core value we identify**. Ensuring that switching costs from Amplenote are zero keeps us honest in our long-term goal to build the best note taking app. We are always improving our exporter, and we welcome ideas for Exporter improvements via our [voting page](https://www.amplenote.com/feature_vote).

## How do I export my notes?

First, you'll want to access the desktop version of Amplenote (it is not currently possible to export your notes via mobile). Navigate to www.amplenote.com and log into your account there, or click the app icon on your desktop if you have it installed.

Next, click your **Account Icon** icon in the upper left corner of Amplenote, then click **Account settings**.

![Clicking the Account Icon in the upper left corner](https://images.amplenote.com/0d6d0a8c-fad0-11ea-a5bc-f200a12bf340/8c195555-7324-4185-8373-2b57a6b1c944.png)

On the **Account Settings** page, click the **Import & Export** tab.

![The Import & Export tab on the Account Settings page](https://images.amplenote.com/dcb18b82-acd5-11e9-892b-0e2a2a872339/a7d83d09-a6e7-44e8-84a2-52daf5d265bf.png)

On the **Import & Export** page, click the **Start Export** button.

![The Start Export button](https://images.amplenote.com/dcb18b82-acd5-11e9-892b-0e2a2a872339/22e8dbcd-9ae9-47dd-b0c3-0209398ca7f7.png)

Amplenote will ask to verify your account credentials, and then process your notes for export. This may take a little time, depending on how many notes and images you have.

![Verifying account credentials while the export is processed](https://images.amplenote.com/dcb18b82-acd5-11e9-892b-0e2a2a872339/0f07f687-f358-4824-b478-f2599c924fe9.png)

Once the export is complete, Amplenote will send a ZIP file containing your notes to the email address registered with your account.

![The exported ZIP file is delivered to your registered email address](https://images.amplenote.com/dcb18b82-acd5-11e9-892b-0e2a2a872339/034cffeb-bdce-462d-8205-14b0ad55ab21.png)

Alternatively, if you refresh the page, you can click to download the ZIP file directly from the **Export history** section of the **Import & Export** page once the file has finished generating.

![Downloading the export directly from the Export history section](https://images.amplenote.com/dcb18b82-acd5-11e9-892b-0e2a2a872339/af102b4a-4ae1-4600-84e9-c05b508545bf.png)

The **Export history** section can also come in handy should you wish to revisit an older export of your notes.

## How will my exported notes be formatted?

Each note will be exported in [markdown](https://en.wikipedia.org/wiki/Markdown) format with the note name becoming the file name. Markdown is a simple format that can be used by a wide variety of plain text editors and markdown viewers.

![Example of an unzipped export folder structure](https://images.amplenote.com/0d6d0a8c-fad0-11ea-a5bc-f200a12bf340/7ded0bef-fc00-4cf7-91c2-02b75ebd13e8.png)

Any images that have been uploaded to Amplenote will be included in the ZIP file, and your note metadata will be packaged into a [YAML Front Matter](https://jekyllrb.com/docs/front-matter/) section, which is designed to maintain links between notes.

![Example note as it appears in Amplenote](https://images.amplenote.com/0d6d0a8c-fad0-11ea-a5bc-f200a12bf340/df15b6fa-af24-466a-8a64-f02967996d91.png)

![The same note exported to markdown with a YAML front matter header](https://images.amplenote.com/0d6d0a8c-fad0-11ea-a5bc-f200a12bf340/98a6b1fe-4973-4c86-a58b-1117f8d6853c.png)

## Links

- [Amplenote's core values blog post](https://www.amplenote.com/blog/core_values_robust_export_fast_cancellation_always_listening)
- [Feature voting page](https://www.amplenote.com/feature_vote)
- [Markdown reference](https://en.wikipedia.org/wiki/Markdown)
- [YAML Front Matter documentation](https://jekyllrb.com/docs/front-matter/)
