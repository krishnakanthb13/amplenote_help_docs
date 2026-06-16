# Plugins

> [← Help Index](../00-index.md)

The Amplenote plugin system: reference docs, creation, actions, interfaces, examples, and appendices.

- [Plugin API Reference Documentation](./developing_amplenote_plugins.md) — Overview of the plugin system and map of the reference documentation.
- [Plugin Creation: settings, name and metadata](./plugin_creation.md) — How to structure a plugin note with a metadata table and code block.
- [Actions: Ways to invoke/initiate plugin execution](./actions.md) — The full list of action hooks (appOption, noteOption, insertText, renderEmbed, etc.) and the optional check function.
- [App interface: Plugin methods to interact with user notes](./app_interface.md) — The `app.*` methods for reading and modifying notes, tasks, tags, and more.
- [Note Interface: Query or perform actions on a note](./note_interface.md) — The single-note `note.*` abstraction for content, tags, tasks, and attachments.
- [Plugin API Examples](./examples.md) — Starter repositories and practical code patterns including LLM integration.
- [Appendix I: Types](./appendix_i.md) — Type definitions for attachment, image, link, noteHandle, task, and others.
- [Appendix II: Plugin code execution environment](./appendix_ii.md) — How plugin code runs in a sandboxed iFrame / WebView.
- [Appendix III: Markdown content](./appendix_iii.md) — Notes on markdown support and limitations for plugins.
- [Appendix IV: Loading external libraries](./appendix_iv.md) — Patterns for loading browser builds and UMD modules.
- [Plugin Markdown Reference](./plugin_api_markdown_reference_parse_markdown.md) — Markdown syntax details: colored text, footnotes, tables, collapsible headings, task objects.
- [Plugin Example: AI Plugin](./example_plugin_ai.md) — The AmpleAI plugin as a worked example: features, providers, configuration.
- [Using the default AmpleAI plugin](./using_default_ai_plugin.md) — End-user guide to AmpleAI features, model list, and backend setup.

> A deeper, per-method version of this plugin reference (one file per action/method) is maintained separately in the sibling `amplenote_references` repository.
