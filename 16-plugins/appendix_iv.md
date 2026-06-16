# Appendix IV: Loading external libraries

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins/appendix_iv)

## Overview

The plugin execution context provides isolation that allows looser restrictions on loading external resources. The documentation outlines two primary patterns for loading external dependencies based on how they're packaged.

## Loading Browser Builds

Browser builds represent the simplest dependency type—libraries designed for standard `<script>` tag usage. In plugin code, a script element can be appended to the document to load such dependencies.

### Example: RecordRTC Library

The documentation provides this implementation pattern:

```javascript
_loadRecordRTC() {
  if (this._haveLoadedRecordRTC) return Promise.resolve(true);
  return new Promise(function(resolve) {
    const script = document.createElement("script");
    script.setAttribute("type", "text/javascript");
    script.setAttribute("src", "https://www.WebRTC-Experiment.com/RecordRTC.js");
    script.addEventListener("load", function() {
      this._haveLoadedRecordRTC = true;
      resolve(true);
    });
    document.body.appendChild(script);
  });
}
```

Key considerations include:
- The plugin context persists, eliminating need for repeated loading
- Browser-build libraries become available as window properties (e.g., `window.RecordRTC`)

### Usage in Plugin Actions

```javascript
async insertText(app) {
  await this._loadRecordRTC();
  // remaining code can reference window.RecordRTC
}
```

## Loading UMD Builds

For UMD module dependencies, a helper function enables loading:

```javascript
async _loadUMD(url, module = { exports: {} }) {
  const response = await fetch(url);
  const script = await response.text();
  const func = Function("module", "exports", script);
  func.call(module, module, module.exports);
  return module.exports;
}
```

### Example Usage

```javascript
async imageOption(app, image) {
  const metaPNG = await this._loadUMD("https://www.unpkg.com/meta-png@1.0.6/dist/meta-png.umd.js");
  // remaining code can use metaPNG.*
}
```
