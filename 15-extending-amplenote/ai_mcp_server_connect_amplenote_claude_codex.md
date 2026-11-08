# Claude & Codex: Enable MCP access to read and write notes on desktop

> [← Help Index](../00-index.md) · Category: [Extending Amplenote](./index.md) · [Source ↗](https://www.amplenote.com/help/ai_mcp_server_connect_amplenote_claude_codex)

## Overview

Amplenote offers an MCP Server connection for Unlimited plan subscribers and above, allowing frontier LLMs like Claude and Codex to read, write, edit, and search notes through a local desktop integration.

## Benefits

The MCP Server enables an AI agent to read, edit, or author any note, table, or task in your account from a separate window. Unlike Ample Agent Pro, this approach runs independently without slowing down your main Amplenote app, making it ideal for long-running commands.

## Installation Steps

### 1. Subscribe to Unlimited or Founder Plan

MCP Server access requires an Unlimited or Founder subscription level.

### 2. Download Desktop App and Enable MCP

- Download and install Ample Desktop
- Open Settings from the desktop app menu
- Toggle the MCP server "on"
- Click the "Copy" button and select your preferred provider (Claude Desktop, Claude Code, or OpenAI Codex)

![Opening settings from macOS after installing](https://images.amplenote.com/e1ba1208-5939-11f1-bbdf-e1e16f5f5509/b411b4d0-8805-4c46-8920-00ee0af17c8c.png)

![MCP toggled on](https://images.amplenote.com/e1ba1208-5939-11f1-bbdf-e1e16f5f5509/d6b21cb1-2188-431c-b78d-220a550b71f1.png)

### 3. Apply Configuration

**Important:** Keep Amplenote Desktop open while using MCP. The copied configuration includes a private bearer token—treat it like a password and never share it publicly.

#### Option A: Claude Desktop

1. Open Claude Desktop and go to Settings > Developer
2. Click "Edit Config"
3. Paste the copied JSON into `claude_desktop_config.json` (macOS: `~/Library/Application Support/Claude/claude_desktop_config.json`; Windows: `%APPDATA%\Claude\claude_desktop_config.json`)
4. If other MCP servers exist, add amplenote as a new entry within the `mcpServers` object
5. Save and completely restart Claude Desktop
6. Verify "amplenote" appears in the MCP/tools indicator

![Editing the Claude Desktop config to add the Amplenote MCP server](https://images.amplenote.com/e1ba1208-5939-11f1-bbdf-e1e16f5f5509/bd97dcff-d6a5-47e5-bdfd-b9a828d30300.png)

![After restarting Claude, you should be able to see "amplenote" among your "Connectors"](https://images.amplenote.com/e1ba1208-5939-11f1-bbdf-e1e16f5f5509/1be5f445-d41c-40cd-8cfd-3cb24f5e2720.png)

#### Option B: Claude Code

1. Ensure Amplenote Desktop is running with MCP enabled
2. Open terminal and paste the copied command
3. Verify with: `claude mcp list` and `claude mcp get amplenote`
4. Start Claude Code with `claude`
5. Run `/mcp` to confirm amplenote is connected

![Successful copy/paste of Claude Code command](https://images.amplenote.com/e1ba1208-5939-11f1-bbdf-e1e16f5f5509/3cceb3be-a186-43cd-9976-4fcd49133d4a.png)

#### Option C: Codex

1. Open Codex's config file at `~/.codex/config.toml`
2. Paste the copied `[mcp_servers.amplenote]` block
3. Save and restart Codex
4. Run `/mcp` to verify amplenote is listed

![Adding the Amplenote MCP server block to the Codex config file](https://images.amplenote.com/e1ba1208-5939-11f1-bbdf-e1e16f5f5509/47068d6d-9707-4676-b3ee-9b77b6217f60.png)

![You should see "amplenote" listed among the MCP entries after typing /mcp](https://images.amplenote.com/e1ba1208-5939-11f1-bbdf-e1e16f5f5509/1430505c-75d3-4cc5-8372-80f6deec3ab6.png)

## Using Amplenote MCP Connector inside an Anthropic organization

If you use a Claude Teams subscription tied to an organization, the default Anthropic `organization` configuration disables Connectors acting without approving each individual action. Fix this in **Organization Settings → "Cowork"** so users can choose "Always allow", which enables "Allow for all tasks" when the MCP server updates multiple notes.

![Organization Settings](https://images.amplenote.com/e1ba1208-5939-11f1-bbdf-e1e16f5f5509/b53ab58d-5dd4-430a-a36d-5cd07f65876d.png)

![Cowork selection](https://images.amplenote.com/e1ba1208-5939-11f1-bbdf-e1e16f5f5509/21d2c1cb-9a5f-42c7-9109-2c3b678b6fe6.png)

## Notes on the local server

`127.0.0.1` means "this same computer" — a cloud-only chatbot, remote server, or different computer cannot reach it. The MCP toggle status shows a green/connected indicator and local URL `http://127.0.0.1:39377/mcp`. Claude Desktop logs MCP connection errors in `~/Library/Logs/Claude` (macOS) and `%APPDATA%\Claude\logs` (Windows).

For Claude Code, the pasted command makes the server available specifically in the project where the command is run; use `--scope user` for a personal connection across projects. Newer Codex versions support streamable HTTP MCP servers with bearer-token auth; the `npx mcp-remote` config is the compatibility-friendly option.

## Verification Checklist

Before using the MCP connection, confirm:

- Amplenote Desktop is open
- MCP toggle is enabled in Settings
- Your LLM app shows amplenote as connected
- Your first instruction explicitly names Amplenote

## Use Case Examples

The MCP Server supports prompts like:

- "Using Amplenote, find my notes about Japan travel and summarize the three most recent ones"
- "Search my Amplenote notes for customer call details from last week and list open tasks"
- "Review all notes tagged 'gitclear/help' and update navigation tab references"
- "Find my Q3 launch plan note and create concrete next-action tasks"

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Amplenote doesn't appear | Verify Desktop is open, MCP toggle enabled, URL matches current settings |
| Claude Desktop shows no MCP indicator | Restart completely; check JSON syntax in config file |
| `npx` not found | Install Node.js LTS; verify with `node --version` and `npx --version` |
| Claude Code command fails | Use proper option order: `claude mcp add --transport http --scope user --header "Authorization: Bearer TOKEN" amplenote http://127.0.0.1:39377/mcp` |
| Connection previously worked, now fails | Re-enable MCP toggle in Amplenote Settings and recopy configuration |
| Codex does not see the server | Ensure the `[mcp_servers.amplenote]` block is not nested inside another TOML table |
| The LLM can read but not write | Approve the tool call, and be explicit (e.g. "Create a new note", "append this markdown") |
| The LLM modifies the wrong note | Ask it to show candidate notes first, then choose |

## Provider Comparison

**Claude Desktop:** Best for conversational note management and task planning; requires JSON configuration.

**Claude Code:** Terminal-first approach; ideal for coding workflows that reference notes or specs.

**Codex:** Uses TOML configuration; shares settings between CLI and IDE extension.
