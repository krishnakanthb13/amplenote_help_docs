# Guide to Building Plugins (Beginner to Advanced)

> [← Help Index](../00-index.md) · Category: [Extending Amplenote](./index.md) · [Source ↗](https://www.amplenote.com/help/guide_to_developing_amplenote_plugins)

## Article Overview

This comprehensive guide explains how to create and modify Amplenote plugins, from complete beginners to advanced developers. The key premise is that plugins are simply notes containing code blocks—no special software or git knowledge required initially.

## Main Sections

### Beginner Path: Writing Basic Code in Notes

Three starting options exist:

1. **Copy a working example** - Duplicate the Example AI plugin via Amplecap
2. **Use the embed repo** - Fork the amplenote-embed-starter project for React components
3. **Build from scratch** - Create any note with a table and code block per API specs

### Iteration & Debugging

**For broken functionality:**

- Use `console.log` statements to output state
- Invoke `debugger` for pausing execution
- Wrap code in `try..catch` blocks

**For compilation problems:**

- Undo changes (Cmd-Z/Ctrl-Z) to working state
- Check DevTools Console for error messages
- Paste code into IDE (VS Code) to spot syntax errors
- Review version history
- Look for missing commas between object methods

### Intermediate-to-Advanced Development

Benefits of using an IDE:

- Instant syntax error visibility
- "Faster iteration" is emphasized as critical
- Step through code with debuggers
- Enhanced stability through testing

**Getting started:**

- Use the "Amplenote Plugin Template repo" on GitHub
- Create test files with mocked plugin/app objects
- Set breakpoints in WebStorm or similar IDEs
- Use the "Github->Amplenote plugin" to auto-sync code changes

### Learning by Example

The guide references several open-source plugins demonstrating key techniques:

- **AI plugin**: OpenAI API calls with configurable settings
- **Readwise plugin**: Third-party REST API with rate limiting
- **Image generation plugin**: Image handling and URL-to-blob conversion
- **Thesaurus**: Radio button selections and simpler API calls
- **Amplequery**: Querying across all notes, filtering, and table generation

### AI-Assisted Code Generation

Phind.com is recommended over standard ChatGPT because it can reference documentation links. The guide provides specific tips:

- Enable the "expert" toggle for GPT-4
- Use "Advanced" mode to paste Amplenote API documentation URL
- Provide follow-up questions to replace libraries that don't work in browser environments
- Use Chrome Inspector's Console to debug returned objects

### Practical Example: Note2PDF Plugin

This real-world case study shows:

- Initial Phind query generated non-working code requiring CDN-compatible libraries
- Follow-up queries replaced `marked` with `showdown` and `pdfkit` with `js2pdf`
- `console.log` statements diagnosed each conversion step (markdown→HTML→PDF)
- Final implementation required consulting official API docs for download functionality

## Developer Incentives

- **Free Unlimited subscriptions** available for plugin developers (email support@amplenote.com)
- **Plugin Bounty Board** offers $20,000+ for building requested plugins
- Sell plugins starting Q1 2025
- Custom support links available on public profiles

## Key Resources Linked

- [Plugin API Documentation](https://www.amplenote.com/help/developing_amplenote_plugins)
- [Published Plugin Directory](https://amplenote.com/plugins)
- [Discord community](https://discord.gg/nAj4wp4sJm)
- [Amplenote Plugin Template](https://github.com/alloy-org/plugin-template)
- [Yappy plugin example](https://github.com/alloy-org/yappy)
- [Phind.com](https://phind.com) for AI code generation
