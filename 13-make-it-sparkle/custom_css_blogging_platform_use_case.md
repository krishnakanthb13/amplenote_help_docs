# Create your own styled blog with instant updating to replace Wordpress

> [← Help Index](../00-index.md) · Category: [Make it Sparkle](./index.md) · [Source ↗](https://www.amplenote.com/help/custom_css_blogging_platform_use_case)

## Overview

Amplenote enables users to publish styled blog posts that update in real time, offering an alternative to traditional blogging platforms. The setup takes approximately 10-15 minutes and involves uploading a custom stylesheet and embedding notes into your blog platform.

![Amplenote styled blog example](https://images.amplenote.com/d833f77c-fb92-11ea-a4f3-1a263ad550a8/53cfa3de-ad44-48b8-8176-6972e2c05c94.jpg)

## Key Benefits

The main advantage is simplified content updates. Rather than logging into WordPress repeatedly to edit and republish, users simply modify notes in Amplenote, and changes propagate instantly to the published blog post.

## SEO Performance

Google successfully indexes embedded Amplenote blog content. The average embed loads in under 500ms, meeting Google's recommended content load times. Real-world examples include GitClear's blog posts that rank well in search results, with content quality being the primary performance determinant.

## Implementation Steps

### 1. Add Custom Stylesheet

A Medium-inspired CSS stylesheet must be hosted on your blog's domain. The stylesheet file (provided in the article) defines styling for `.ample-editor.readonly` elements, covering typography, spacing, blockquotes, and responsive design.

A dark-theme alternative stylesheet is also available.

### 2. Upload Stylesheet to Host

Using your hosting provider's File Manager or FTP tool (typically within cPanel):
- Navigate to a public directory
- Upload the CSS file (e.g., `blog_style.css`)
- Note the full URL path (e.g., `https://www.my-web-domain.com/stylesheets/blog_style.css`)

![Uploading the stylesheet via cPanel File Manager](https://images.amplenote.com/0ccdc888-8274-11eb-a787-162dd8902ef3/b6952afc-a967-4bf9-8879-27568deb3a38.png)

![Navigating to a public directory to upload the CSS file](https://images.amplenote.com/0ccdc888-8274-11eb-a787-162dd8902ef3/31eddc44-64bf-4883-b2f2-482d40a16cb4.png)

### 3. Configure Amplenote Embed

In Amplenote's "Embed Note Content" dialog, enter the stylesheet URL path in the appropriate field.

![Configuring the Amplenote embed note options](https://images.amplenote.com/0ccdc888-8274-11eb-a787-162dd8902ef3/abbf3200-d0ae-4a4a-b465-142bd14a3ad1.png)

### 4. Publish to Blog Platform

Copy the HTML from Amplenote's embed dialog and paste it into your blogging platform (WordPress requires changing the block type to "Custom HTML"). Publish, and the note becomes a live-updating blog post.

![Selecting the Custom HTML block in WordPress](https://images.amplenote.com/0ccdc888-8274-11eb-a787-162dd8902ef3/dc8dad80-295b-4a53-b144-04320b386770.png)

![Pasted HTML embed result in WordPress](https://images.amplenote.com/0ccdc888-8274-11eb-a787-162dd8902ef3/6d9081d6-e19d-400a-af35-6eee2052e10e.png)

## Performance Characteristics

Amplenote uses server-side CDN caching with a 2-hour time-to-live. While initial requests take 350-500ms, subsequent visitors within the cache window receive content from edge nodes at significantly faster speeds, without relying on client-side caching.

## Example Blogs

- GitClear blog (since 2019)
- bill.harding.blog
- Noteapps.info blog
- Amplenote's own blog
