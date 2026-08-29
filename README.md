# Vivia plugins

This repository contains installable Vivia plugins for Claude Code, Codex,
Cursor, and Antigravity. The canonical repository is
`https://github.com/hey-vivia/plugins`. The hosted MCP endpoint is
`https://app.heyvivia.com/api/mcp`.

Add this repository as a marketplace in your client:

```text
claude plugin marketplace add hey-vivia/plugins
claude plugin install vivia@vivia

codex plugin marketplace add hey-vivia/plugins
codex plugin add vivia@vivia
```

The client-specific directories under `plugins/` use the Claude Code files as
their source. Repository checks compare these directories, so every client
receives the same Vivia behavior.

All four plugin manifests use one version. Release-please manages plugin
releases. Plugin versions are separate from the hosted service.
