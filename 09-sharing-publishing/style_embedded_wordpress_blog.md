# Styling a blog for use with embedded notes

> [← Help Index](../00-index.md) · Category: [Sharing & Publishing](./index.md) · [Source ↗](https://www.amplenote.com/help/style_embedded_wordpress_blog)

## Use case overview

This guide explains how to "Create your own CSS styled blog with Amplenote to replace Wordpress" by publishing notes with custom styling that replicates Medium.com's aesthetic. The setup takes approximately 10-15 minutes.

## SEO performance

Google can index embedded content fully. The document notes that "the average embed loads in less than 500ms, which is well within the range of content load times recommended by Google." Content quality remains the primary performance determinant.

## Real-world examples

Four blogs use this approach: GitClear (since 2019), bill.harding.blog, Noteapps.info, and Amplenote's own blog.

## Key benefit

Updates happen immediately — editing a note automatically updates the live blog post without logging into WordPress repeatedly.

## Technical implementation

1. Add a custom CSS stylesheet to your blog host.
2. Use File Manager or FTP to upload the stylesheet file.
3. Enter the stylesheet URL in Amplenote's embed dialog.
4. Paste the HTML into WordPress as a Custom HTML block.
5. Publish.

## Performance details

Content is served via CDN caching with a 2-hour time-to-live, enabling sub-200ms load times for repeat visitors through server-side optimization.
