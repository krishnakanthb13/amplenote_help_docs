# Why is my uploaded image showing as a gray box?

> [← Help Index](../00-index.md) · Category: [Devices & Syncing](./index.md) · [Source ↗](https://www.amplenote.com/help/image_upload_problems_debug)

If you're here, you probably want to paste an image into a note, but all you're getting is a gray box. As Amplenote continues to evolve, we will improve our error messaging for situations where images cannot be successfully processed. In the meantime, please consider whether any of the following circumstances might apply to the image you're looking to insert.

## 1. You copied an image with a URL that Amplenote can't access

Aka "The Slack gray box" problem. Certain services, like Slack and Jira, host images that can not be viewed without being logged in. To understand this problem, it helps to recognize the distinction between an "image uploaded to Amplenote" and "an HTML `img` tag." Either of these can be pasted into a note. The benefit of pasting in an image with a URL is that it can dynamically update. The drawback is that 1) HTML `img` tags do not have OCR applied to them (since Amplenote doesn't possess their content) 2) if the user is viewing the note from a context where their browser doesn't have access to the URL (e.g., because you're not logged in to Slack in Chrome), you get a gray box.

**Solution**: Usually the easiest way to solve this is to download the image to your computer, then upload to Amplenote so your image will be available from any viewing context.

## 2. You uploaded a file from a privileged macOS directory ("Downloads" or "Desktop") without giving access

macOS requests special permission for the browser to access files in directories that are known to contain user content. If at some point you deny your browser access to a certain folder, then subsequent files chosen for upload from that folder will result in failed image uploads.

**Solution**: [Apple has a help page with instructions on how to control which folders can be accessed by which applications](https://support.apple.com/guide/mac-help/control-access-to-files-and-folders-on-mac-mchld5a35146). Assuming you have installed the Amplenote PWA in Chrome, [this is what your Privacy settings should look like](https://images.amplenote.com/e05df9f8-0a9e-11ed-b1de-b244f95defbd/a0a757e7-2c38-457e-8055-5194f2a654bc.png).

## 3. You uploaded an unsupported content type [speculative]

Accepted image content types in Amplenote include `image/bmp`, `image/gif`, `image/jpeg`, `image/jpg`, `image/png`, `video/mp4`, `video/mpeg`, `video/quicktime`, `video/webm`. If you try to upload some other type of image or video, you will not succeed.

Also note that there are limits to image size based on subscription level. Subscribers on the free Personal plan can only upload images less than 5mb in size.

**Solution**: Export the content to one of the supported formats and re-upload.

## 4. You have ambiguous internet access [speculative]

Aka the "Connected to Boingo wifi on the plane without paying" problem. When your system believes that you are connected to wifi, but you can't actually access any network resources because you're behind a firewall, it's not possible for Amplenote to upload images.

**Solution:** Disconnect from the unusable wifi. Images uploaded offline will be queued for upload next time you connect to usable wifi.
