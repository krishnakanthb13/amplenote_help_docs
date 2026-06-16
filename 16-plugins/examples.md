# Plugin API Examples

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins/examples)

## Page Overview

This documentation page serves as a resource for plugin developers, providing practical examples and code snippets for building Amplenote plugins.

## Starter Repositories

The page recommends three primary starting points:

- **Plugin Embed Starter Project**: A React-based application framework for rendering plugins in notes and sidebars
- **Plugin Template**: A minimal plugin with testing capabilities
- **Existing Plugins**: Over 100 community plugins available as reference implementations

## Key Examples Provided

### Task Action via Slash Command

The documentation illustrates how to implement conditional slash commands for tasks using the `check` method within the `appOption` section. The example demonstrates accessing task properties through `app.context.taskUUID` and the `getTask()` method.

### Parsing Rich Footnotes

An example shows how task content with rich footnotes (including images, links, and connected tasks) is formatted in markdown, with footnote references handled through standard markdown syntax.

### External Service Integration

The page notes that plugins can use `fetch()` to call external APIs, though some services may implement CORS restrictions. It recommends using Cloudflare Workers as a proxy solution for CORS-restricted endpoints.

### LLM Integration

The documentation provides a detailed code example for calling AI providers (OpenAI, Gemini, Anthropic). Key features include:

- Request timeout implementation using `Promise.race()`
- Provider-specific endpoint configuration
- Streaming capability support
- JSON response formatting options

The AmpleAI plugin serves as a reference implementation for these patterns.
