---
name: connect-to-skilder
description: Connect this agent to the user's Skilder workspace over MCP with a browser OAuth sign-in. Checks whether Skilder is already connected, asks once before adding the server to the MCP client configuration, then reports the roles and skills the workspace publishes. Trigger on "connect to Skilder", "set up Skilder", "add the Skilder MCP server".
version: 2.0.0
homepage: https://github.com/skilder-ai/skills
metadata:
  endpoint: https://app.skilder.ai/mcp
  transport: streamable-http
  auth: OAuth 2.1 with browser consent
  operator: skilder.ai SA
---

Connect this agent to the user's Skilder workspace. One endpoint, one browser sign-in, no workspace name or key to collect.

## What the connection is

| | |
|---|---|
| Server | `https://app.skilder.ai/mcp`, Streamable HTTP, operated by skilder.ai SA ([privacy](https://www.skilder.ai/en/privacy), [terms](https://www.skilder.ai/en/terms)). |
| Sign-in | The first request opens a browser page on app.skilder.ai. The user signs in, picks one workspace and presses Approve. Nothing is granted before that press. |
| Credential | Issued to the MCP client after approval and stored by the client. This agent never sees, stores or forwards it. |
| What flows out | The tool calls this agent makes against the chosen workspace, recorded there for the workspace admins. |
| What flows in | The roles and skills the workspace's own admins published for it. Workspace content, available only after approval. |
| Revoke | Remove the server entry from the client configuration. The stored grant expires on its own within 14 days. |

## Step 0: already connected?

Skip to Step 3 when the tool list already contains Skilder's session tool:

```
init_skilder
```

## Step 1: confirm once

Tell the user which command or configuration file will add the server, and that the first request opens a browser sign-in. Continue when they agree. That is the only question: there is no workspace name, link or key to ask for.

## Step 2: add the server

Use the client's own mechanism. The entry is the same everywhere.

```bash
# Claude Code
claude mcp add skilder-ai --transport http https://app.skilder.ai/mcp

# Codex
codex mcp add skilder-ai --url https://app.skilder.ai/mcp
```

Clients configured by file (`.mcp.json`, Cursor's `~/.cursor/mcp.json`, VS Code's `.vscode/mcp.json`, `claude_desktop_config.json`) take this entry under the host's own top-level key (`mcpServers` on most hosts, `servers` on VS Code):

```json
"skilder-ai": {
  "type": "http",
  "url": "https://app.skilder.ai/mcp"
}
```

A client with no way to configure MCP servers cannot connect. State that and stop.

## Step 3: sign in and report

The first request to the server (listing its tools is enough) redirects to the browser sign-in, which the user completes. Then report what the workspace publishes: its roles and, under each, the skills available to this agent.

## Fallback: no browser redirect

A client that cannot follow a browser redirect connects with a key instead, from Skilder's Connect page → Advanced. The key comes from the user.
