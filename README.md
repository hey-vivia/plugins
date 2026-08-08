# Vivia plugins

This repository contains installable Vivia plugins for Claude Code, Codex,
Cursor, and Antigravity. The canonical repository is
`https://github.com/hey-vivia/plugins`. The hosted MCP endpoint is
`https://app.heyvivia.com/api/mcp`.

Add this repository as a marketplace in the client you use:

```text
claude plugin marketplace add hey-vivia/plugins
claude plugin install vivia@vivia

codex plugin marketplace add hey-vivia/plugins
codex plugin add vivia@vivia
```

The client-specific directories under `plugins/` use the Claude Code files as
their source. The repository checks these directories together, so all clients
receive the same Vivia behavior.

All four plugin manifests use the same version. This repository manages plugin
releases with release-please. Plugin versions are separate from the hosted
service.
