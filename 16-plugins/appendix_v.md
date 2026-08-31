# Appendix V: CORS Proxy

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins/appendix_v)

## Overview

Plugin code runs in a sandboxed web origin, so any request a plugin makes with `fetch` is subject to the browser's same-origin policy. Servers that don't return permissive CORS headers for the plugin sandbox origin will cause those requests to fail. To work around this, Amplenote provides a CORS proxy that forwards a request to a target URL and re-emits the response with CORS headers that the plugin sandbox accepts.

## Allowlist

The proxy only forwards requests to a fixed allowlist of upstream hostnames. Requests for any other host return `400 Bad Request` without contacting the upstream. The current allowlist is:

- `actions.zapier.com`, `mcp.zapier.com`
- `api.assemblyai.com`
- `api.track.toggl.com`
- Any single-segment subdomain of `atlassian.net` (e.g. `your-workspace.atlassian.net`)
- `github.com`
- `raw.githubusercontent.com`
- `images.amplenote.com`, `images-dev.amplenote.com`, `www.amplenote.com`
- `public.amplenote.com`
- `ample-attachments.s3.us-west-2.amazonaws.com`, `ample-attachments-dev.s3.us-west-2.amazonaws.com`
- Any subdomain of `pinecone.io`
- `readwise.io`
- `search.projectsegfau.lt`
- `storage.googleapis.com`

If a plugin needs to talk to a host that isn't on this list, the host must be added to the allowlist before the request will succeed. Contact `support@amplenote.com` to request a host be added to the list.

## URL

The proxy is hosted at: `https://plugins.amplenote.com/cors-proxy`

## Query parameters

- `apiurl` — the `String` URL of the upstream resource to fetch. The proxy issues a request to this URL and returns its response to the plugin.

## Request forwarding

The proxy forwards the HTTP method, request body, and headers from the plugin's `fetch` call to the upstream URL. This means a plugin can:

- Issue `GET`, `POST`, or other methods by setting the `method` option on `fetch`
- Send a request body (e.g. JSON) by setting the `body` option on `fetch`
- Send authorization or content-type headers by setting the `headers` option on `fetch`

The proxy returns the upstream response's status, body, and content type back to the plugin, with CORS headers added so the response can be read.

## Examples

### Fetching binary content

Useful for downloading images or other binary resources that don't serve CORS headers to the plugin origin.

```javascript
async noteOption(app, noteUUID) {
  const images = await app.getNoteImages({ uuid: noteUUID });
  if (images.length === 0) return;
  const proxyURL = new URL("https://plugins.amplenote.com/cors-proxy");
  proxyURL.searchParams.set("apiurl", images[0].src);
  const response = await fetch(proxyURL);
  const buffer = await response.arrayBuffer();
  // ...do something with the binary content
}
```

### POSTing JSON to a third-party API

Useful for calling APIs that require an `Authorization` header and accept a JSON body but don't serve CORS headers for the plugin origin.

```javascript
async appOption(app) {
  const apiKey = app.settings["API Key"];
  if (!apiKey) throw new Error("API Key is required");
  const proxyURL = new URL("https://plugins.amplenote.com/cors-proxy");
  proxyURL.searchParams.set("apiurl", "https://api.example.com/v1/resource");
  const response = await fetch(proxyURL, {
    body: JSON.stringify({ expires_in: 3600 }),
    headers: { "Authorization": apiKey, "Content-Type": "application/json" },
    method: "POST",
  });
  const result = await response.json();
  // ...do something with the response
}
```

### Fetching text content (e.g. an HTML page)

Useful for scraping, polling, or otherwise inspecting the textual content of a page.

```javascript
async appOption(app) {
  const proxyURL = new URL("https://plugins.amplenote.com/cors-proxy");
  proxyURL.searchParams.set("apiurl", "https://www.amplenote.com/plugins?sort_by=newest");
  const response = await fetch(proxyURL);
  const text = await response.text();
  const div = document.createElement("div");
  div.innerHTML = text;
  // ...inspect the parsed DOM
}
```

## Notes

- The `apiurl` query parameter must be set on the proxy URL; requests without it will not reach an upstream server.
- The proxy does not modify the upstream payload — the response a plugin sees has the same body and content type the upstream returned.
- Attachment URLs returned by `app.getAttachmentURL(...)` are served from a host that does not include CORS headers for the plugin origin, so reading attachment content from a plugin requires going through this proxy. See `Example: reading attachment content` in the App Interface documentation for an end-to-end example.

## Related

- [App interface](./app_interface.md) — see "reading attachment content" example for a full CORS proxy workflow
- [Appendix IV: Loading external libraries](./appendix_iv.md) — loading external code libraries (vs. fetching data)
