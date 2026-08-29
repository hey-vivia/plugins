# Vivia plugin distribution

This repository is the public package source for Vivia plugins across supported clients, including Claude Code, Codex, Cursor, and Antigravity.

It is intended to be a distribution and validation repository, not the application runtime itself. The public plugin content here is the canonical source for installable plugin packages, and each platform-specific folder is kept in sync with the shared Vivia behavior and metadata.

## Public source

- Website: https://heyvivia.com/
- Documentation: https://docs.heyvivia.com/
- Repository: https://github.com/hey-vivia/plugins
- Hosted MCP endpoint: https://app.heyvivia.com/api/mcp

## What this repo contains

- canonical Vivia instructions and agent definitions for the Claude Code reference implementation
- platform-specific copies for Codex, Cursor, and Antigravity
- marketplace metadata and manifests for each supported client
- release/version metadata for plugin distribution
- validation checks that keep the public package consistent and prevent leaking app-specific or local runtime details

## Plugin structure

```text
plugins/
  claude-code/
  codex/
  cursor/
  antigravity/
```

The platform directories are generated and checked against the canonical content so each client receives the same behavior and configuration while adapting for client-specific naming and tool conventions.

## Installing from this package

Use your client’s marketplace or plugin installation flow to add this repository and install the `vivia` plugin package.

Examples:

```text
claude plugin marketplace add hey-vivia/plugins
claude plugin install vivia@vivia

codex plugin marketplace add hey-vivia/plugins
codex plugin add vivia@vivia
```

The exact commands can vary slightly by client version and tooling, but the repository is the public source of truth for the Vivia plugin distribution.

## Validation and sync

This repo includes a guardrail script to ensure the public distribution stays consistent.

```bash
bun run check
bun run sync
```

- `bun run check` validates manifest/version alignment, drift, and public-boundary rules.
- `bun run sync` applies safe auto-fixes for synced plugin content.

## Release model

- All plugin manifests share the same public version number.
- Releases are managed with release automation for the plugin package.
- The plugin package version is separate from the hosted Vivia service itself.

## Important boundary

This repository is for public plugin distribution and integrity checks. It should not contain app runtime code, deployment config, local workstation endpoints, or private service credentials.
