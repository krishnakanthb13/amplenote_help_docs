# Plugin Creation: settings, name and metadata

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins/plugin_creation)

## Overview

To create an Amplenote plugin, you need a note containing two components: a metadata table with plugin information and a code block with JavaScript implementation.

## Metadata Table

The metadata table requires at least two columns: setting name and setting value. All entries are interpreted as strings, and setting names are case-insensitive.

![Example plugin metadata table](https://images.amplenote.com/2ae961e0-bc5d-11ed-808b-e21efa2d8566/c7582134-fdf7-431e-9f7d-85d8f73c01dd.png)

### Required Setting

**name** — The only mandatory field. This name appears when users invoke the plugin and serves as a prefix for multiple options.

### Optional Settings

**icon** — References a Material Design Icon to identify the plugin. Defaults to a generic extension icon if omitted.

**description** — A brief explanation displayed during plugin installation or configuration.

**instructions** — Detailed guidance for plugin usage, shown if published to the Plugin Directory.

**setting** — Defines configurable parameters accessible to plugin code via `app.settings`. Can be repeated for multiple settings, with all values provided as strings.

## Code Block

The first code block in the note becomes the plugin's JavaScript code. Subsequent blocks are ignored. The code should export a JavaScript object with functions matching action names.

### Action Structures

Actions can be:
- Simple functions
- Objects with multiple named actions
- Objects with `check` and `run` functions for validation and execution

### Features

- Plugin object persists as `this` with state retention
- Functions receive `app` as the first argument for accessing settings
- Action functions support promises and async/await syntax
- Additional action-specific arguments follow the `app` parameter

### Example Structure

```javascript
{
  insertText(app) {
    return "Hello World!"
  }
}
```

Multiple actions with validation:

```javascript
{
  insertText: {
    check(app) {
      return true;
    },
    run(app) {
      return "Hello World!";
    }
  }
}
```

## Accessing Settings

Settings defined in the metadata table are accessible through `app.settings["Setting Name"]`.

## Large plugins: keeping the payload out of the code block

The first code block in the note is still required and defines the plugin's actions. But for large payloads (a compiled embed document, a client bundle, or a large data file), you can upload them as attachments on the plugin note instead of inlining them into the code block.

```javascript
async renderEmbed(app) {
  if (app.context.setEmbedHTML) {
    app.context.setEmbedHTML(`<!-- spinner markup -->`); // paint before awaiting network
  }
  try {
    const attachments = await app.getNoteAttachments(app.context.pluginUUID);
    const attachment = attachments.find(attachment => attachment.name === "build.html.json");
    if (!attachment) throw new Error("build.html.json attachment not found");
    return this._getAttachmentContent(app, attachment.uuid);
  } catch (error) {
    return `<div><em>renderEmbed error:</em> ${ error.toString() }</div>`;
  }
},

async _getAttachmentContent(app, attachmentUUID) {
  const url = await app.getAttachmentURL(attachmentUUID);
  const proxyURL = new URL("https://plugins.amplenote.com/cors-proxy");
  proxyURL.searchParams.set("apiurl", url);
  const response = await fetch(proxyURL);
  return response.text();
}
```

**Key considerations:**
- Requires an online client because `getAttachmentURL` mints a temporary URL.
- The attachment reference must stay referenced in the note body.
