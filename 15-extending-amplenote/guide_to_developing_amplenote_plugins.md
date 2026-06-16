# Guide to Building Plugins (Beginner to Advanced)

> [← Help Index](../00-index.md) · Category: [Extending Amplenote](./index.md) · [Source ↗](https://www.amplenote.com/help/guide_to_developing_amplenote_plugins)

## Article Overview

This comprehensive guide explains how to create and modify Amplenote plugins, from complete beginners to advanced developers. The key premise is that plugins are simply notes containing code blocks—no special software or git knowledge required initially.

## Main Sections

### Beginner Path: Writing Basic Code in Notes

Three starting options exist:

1. **Copy a working example** - Duplicate the Example AI plugin via Amplecap

![Copying a working example plugin to start from](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/bd3c348e-bf39-4cd9-8eb8-701ce2891540.png)
2. **Use the embed repo** - Fork the amplenote-embed-starter project for React components
3. **Build from scratch** - Create any note with a table and code block per API specs

### Iteration & Debugging

**For broken functionality:**

- Use `console.log` statements to output state
- Invoke `debugger` for pausing execution
- Wrap code in `try..catch` blocks

![Iterating on your plugin as you go](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/81fc498e-e2ab-4281-a2fc-ee8499cbce28.png)

![Iterating on your plugin as you go](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/91599d8e-703d-4865-b7b1-241aa9c9c641.png)

![Iterating on your plugin as you go](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/97d25a35-9042-4995-b75b-b5c2edc64661.png)

![Iterating on your plugin as you go](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/aa3011fc-875f-40a9-b23b-ba48e3c25117.png)

**For compilation problems:**

- Undo changes (Cmd-Z/Ctrl-Z) to working state
- Check DevTools Console for error messages
- Paste code into IDE (VS Code) to spot syntax errors
- Review version history
- Look for missing commas between object methods

![Diagnosing a plugin compilation problem](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/5750d8a6-93e6-406c-81a1-6b74e93bd976.png)

![Diagnosing a plugin compilation problem](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/16d5b882-d944-4fb2-87b8-f4a4a966839c.png)

![Diagnosing a plugin compilation problem](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/291e1f7c-9eb6-4fb6-9803-af3f71a4bb46.png)

![Diagnosing a plugin compilation problem](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/cb2932c9-92c6-4f9c-8ebc-2bf5cb6bc3db.png)

![Diagnosing a plugin compilation problem](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/dae6b674-9143-4ea5-8a66-77048978c620.png)

### Intermediate-to-Advanced Development

Benefits of using an IDE:

- Instant syntax error visibility
- "Faster iteration" is emphasized as critical
- Step through code with debuggers
- Enhanced stability through testing

![Developing a plugin in an IDE](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/f7c28bee-2cbf-4a0d-bcd6-7c9d1d8363da.png)

**Getting started:**

- Use the "Amplenote Plugin Template repo" on GitHub
- Create test files with mocked plugin/app objects
- Set breakpoints in WebStorm or similar IDEs
- Use the "Github->Amplenote plugin" to auto-sync code changes

![Getting started with the example plugin repo](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/9556ee86-e888-43e9-bf57-0303bc86ed08.png)

### Learning by Example

The guide references several open-source plugins demonstrating key techniques:

- **AI plugin**: OpenAI API calls with configurable settings
- **Readwise plugin**: Third-party REST API with rate limiting
- **Image generation plugin**: Image handling and URL-to-blob conversion
- **Thesaurus**: Radio button selections and simpler API calls
- **Amplequery**: Querying across all notes, filtering, and table generation

![Learning by example from open-source plugins](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/14d3df44-5320-4592-865b-59a4d20c4794.png)

### AI-Assisted Code Generation

Phind.com is recommended over standard ChatGPT because it can reference documentation links. The guide provides specific tips:

- Enable the "expert" toggle for GPT-4
- Use "Advanced" mode to paste Amplenote API documentation URL
- Provide follow-up questions to replace libraries that don't work in browser environments
- Use Chrome Inspector's Console to debug returned objects

![Letting AI generate plugin code](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/b5b81595-4d8d-4fc6-8fd3-09400161d585.png)

![Letting AI generate plugin code](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/9e5405e8-eb76-41dc-a085-6f15840bbe01.png)

### Practical Example: Note2PDF Plugin

This real-world case study shows:

- Initial Phind query generated non-working code requiring CDN-compatible libraries
- Follow-up queries replaced `marked` with `showdown` and `pdfkit` with `js2pdf`
- `console.log` statements diagnosed each conversion step (markdown→HTML→PDF)
- Final implementation required consulting official API docs for download functionality

![Building the Note2PDF plugin](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/50a1c807-c14d-4f75-9389-37a1383ed9aa.png)

![First version of Note2PDF plugin, as generated by AI](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/fb4858b5-b953-4697-bbc6-9973f058b7fb.png)

![Building the Note2PDF plugin](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/2484108f-07cf-498c-a2f1-79bf94a83fe9.png)

![Building the Note2PDF plugin](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/8341d764-8cc1-44f1-977a-619c5b3f81be.png)

![Building the Note2PDF plugin](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/97033a72-fcf1-4136-ade2-966b318eac9a.png)

![Upon inserting console.log statements, you can view the 'Console' tab in Chrome Inspector to see what objects are being returned by libraries](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/869e1257-e2d0-4102-a420-156603be757c.png)

![Viewing Javascript variables as revealed by console.log](https://images.amplenote.com/b456a2e4-d93b-11ed-b6ce-f2e3384d8128/3055bd72-c48a-4246-a65a-6768de65fc81.png)

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
