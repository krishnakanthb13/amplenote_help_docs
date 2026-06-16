# Styling a blog for use with embedded notes

> [← Help Index](../00-index.md) · Category: [Sharing & Publishing](./index.md) · [Source ↗](https://www.amplenote.com/help/style_embedded_wordpress_blog)

## Use case overview

This guide explains how to "Create your own CSS styled blog with Amplenote to replace Wordpress" by publishing notes with custom styling that replicates Medium.com's aesthetic. The setup takes approximately 10-15 minutes.

![Example of a CSS-styled blog built with Amplenote embedded notes](https://images.amplenote.com/d833f77c-fb92-11ea-a4f3-1a263ad550a8/53cfa3de-ad44-48b8-8176-6972e2c05c94.jpg)

## SEO performance

Google can index embedded content fully. The document notes that "the average embed loads in less than 500ms, which is well within the range of content load times recommended by Google." Content quality remains the primary performance determinant.

## Real-world examples

Four blogs use this approach: GitClear (since 2019), bill.harding.blog, Noteapps.info, and Amplenote's own blog.

## Key benefit

Updates happen immediately — editing a note automatically updates the live blog post without logging into WordPress repeatedly.

## Technical implementation

1. Add a custom CSS stylesheet to your blog host.
2. Use File Manager or FTP to upload the stylesheet file.

![Uploading the stylesheet file using the cPanel File Manager interface](https://images.amplenote.com/0ccdc888-8274-11eb-a787-162dd8902ef3/b6952afc-a967-4bf9-8879-27568deb3a38.png)

![Public directory structure within the File Manager](https://images.amplenote.com/0ccdc888-8274-11eb-a787-162dd8902ef3/31eddc44-64bf-4883-b2f2-482d40a16cb4.png)

3. Enter the stylesheet URL in Amplenote's embed dialog.

![Configuring the Embed Note Content dialog with the stylesheet URL](https://images.amplenote.com/0ccdc888-8274-11eb-a787-162dd8902ef3/abbf3200-d0ae-4a4a-b465-142bd14a3ad1.png)

4. Paste the HTML into WordPress as a Custom HTML block.

![Selecting the Custom HTML block in WordPress](https://images.amplenote.com/0ccdc888-8274-11eb-a787-162dd8902ef3/dc8dad80-295b-4a53-b144-04320b386770.png)

![Pasted HTML content shown in the WordPress editor](https://images.amplenote.com/0ccdc888-8274-11eb-a787-162dd8902ef3/6d9081d6-e19d-400a-af35-6eee2052e10e.png)

5. Publish.

## Performance details

Content is served via CDN caching with a 2-hour time-to-live, enabling sub-200ms load times for repeat visitors through server-side optimization.
