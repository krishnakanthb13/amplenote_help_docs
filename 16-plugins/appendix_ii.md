# Appendix II: Plugin code execution environment

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins/appendix_ii)

## Overview

"Plugin code is executed in a sandboxed iFrame, preventing direct access to the outer page/application." On mobile platforms, plugins run in isolated WebViews with separation between different plugin instances.

## Browser Compatibility

The execution environment operates within users' browsers (web) or system WebViews (mobile). Importantly, "There are no polyfills applied in the plugin code sandbox, nor is any processing performed on plugin code," meaning developers should account for native browser capabilities without relying on compatibility enhancements.

## Key Points

- **Web**: Plugins execute in the user's browser
- **Mobile**: Plugins load in isolated WebView environments
- **Isolation**: Each plugin iFrame provides separation from other loaded plugins
- **No Processing**: Code runs without polyfills or preprocessing

## Embed Environment

Embeds operate in separated iFrames with additional functions defined on `window`:

### window.callAmplenotePlugin
Calls the `onEmbedCall` action in the host plugin, passing provided arguments. Returns a Promise resolving to the plugin's return value.

### window.setAmplenoteEmbedHeight
Sets a fixed pixel-based height for the embed iframe, overriding aspect-ratio based height while keeping width at 100%. Must be called with a number greater than zero.
