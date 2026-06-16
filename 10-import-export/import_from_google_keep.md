# Importing from Google Keep

> [← Help Index](../00-index.md) · Category: [Import & Export](./index.md) · [Source ↗](https://www.amplenote.com/help/import_from_google_keep)

This article will describe how Amplenote can import data from an existing Google Keep account.

Google offers a comprehensive help page on exporting data. That page was used as reference for the following instructions. If you have any details getting your data downloaded, we recommend checking the most updated version of that help page.

## Step-by-Step Instructions

1. Login to your Google account, and visit [Google Takeout](https://takeout.google.com/?pli=1)
2. By default, all your Google Accounts are selected for download. If you only want to download your Google Keep data, click the "Deselect all" link.
3. Scroll down to "Keep" in the list. The page is alphabetized, which puts "Keep" around the middle of the page. Click the checkbox if it's not already checked.

   *[Screenshot showing Keep checkbox selection]*

![Selecting the Keep checkbox in Google Takeout](https://images.amplenote.com/60d56670-b280-11eb-a645-7e96a2cff41c/ebc1bd1e-7765-4cb5-afa5-9c61a2df8c8e.png)

4. Scroll to the bottom of the page and choose "Next step"

![Choosing "Next step" at the bottom of the page](https://images.amplenote.com/60d56670-b280-11eb-a645-7e96a2cff41c/94a97ecc-7b06-45cb-b119-a37dbde04202.png)

5. Choose how you want to receive your export file from the options provided

![Choosing how to receive your export file](https://images.amplenote.com/60d56670-b280-11eb-a645-7e96a2cff41c/8160d3a1-d63f-4317-9ca4-687da3e7629a.png)
6. Download and unzip your export file (usually a file can be unzipped by double-clicking the downloaded file in your file browser, or by right clicking and choosing "Extract here").

## File Structure and Format Selection

At this point in the process you decide what you want to import to Amplenote.

As of May 2021, a downloaded and unzipped Google Takeout file is structured as a folder called `Takeout` that contains a subfolder called `Keep`. Inside the `Keep` folder are all of the notes that you made in Keep, in multiple file formats. The file format imported by Amplenote is known as "markdown." Markdown files are those that end with the file extension `.md`. When you look in the `Keep` folder, you'll see markdown files mixed among other file types. You can usually separate out just the markdown files by sorting your files by "Kind":

*[Screenshot showing file sorting by Kind]*

![Sorting files by "Kind" to separate the markdown files](https://images.amplenote.com/60d56670-b280-11eb-a645-7e96a2cff41c/7d3bd918-4dad-49cd-95d0-7b752bc4c7a8.png)

## Converting HTML Files to Markdown

As of May 2021, Amplenote supports importing from markdown, but not HTML (want us to import from HTML? Suggest it on our feature voting board and we can get it done! It wouldn't be that much work to build an HTML importer based on our existing markdown importer, but users haven't requested it). So you'll need to convert the HTML files that you want to import into markdown. The easiest way we know of to accomplish this is to first create a zip file with just the images and HTML files you want to import. On macOS it will look something like this:

*[Screenshot showing macOS zip file creation]*

![Creating a zip file of images and HTML files on macOS](https://images.amplenote.com/60d56670-b280-11eb-a645-7e96a2cff41c/f9ab0e9d-c614-428e-8a73-88b1162c50f8.png)

This will create a zip file that has all of the notes as HTML files. At this point, you can use a tool like [Aspose to convert your zipped HTML files to markdown](https://products.aspose.app/html/en/conversion/zip-to-md). We've had mixed results with the quality of the conversion for large zip files. If you find that the markdown you can get from that tool isn't imported correctly into Amplenote, you can instead Google "convert HTML to markdown" and upload the individual HTML notes to get them converted to markdown files. [This looks like one free service](https://www.browserling.com/tools/html-to-markdown) that might be good for converting individual HTML files to markdown.

Once you have converted your HTML notes into markdown (`.md`) files, create a zip file of those markdown notes. The rest is pretty easy.

## Importing to Amplenote

Log in to your Amplenote account, and visit Account Settings -> Import & Export -> Import Markdown

*[Screenshot showing Import Markdown interface]*

![Visiting Account Settings, Import & Export, Import Markdown in Amplenote](https://images.amplenote.com/60d56670-b280-11eb-a645-7e96a2cff41c/3c5871bb-967d-4f8a-850b-19e356b9fbd5.png)

On the ensuing page, click "Choose a markdown or zip file" and select the zip file you created with markdown files
