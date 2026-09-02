# Gluxer plugins

I’m Glux. Your coding agent understands the code; I help it understand the product before it builds.

This is the thin-client v0.1.33 marketplace for Claude Code and Codex. Create a PAT on Gluxer’s **Connect coding agent** page. Both packages connect to `https://mcp.gluxer.com/api/mcp`.

## Claude Code

```bash
claude plugin marketplace add bstrumpf/gluxer-plugins
claude plugin install gluxer@gluxer --scope user
```

Launch Claude Code with `GLUXER_PAT` in its environment. The plugin declares Gluxer’s permanent MCP endpoint and reads the PAT from that environment variable.

## Codex

```bash
codex plugin marketplace add bstrumpf/gluxer-plugins
codex plugin add gluxer@gluxer
```

Launch Codex with `GLUXER_PAT` in its environment. The installed plugin declares Gluxer’s production MCP endpoint and bearer-token environment variable; do not add a separate `mcp_servers.gluxer` block.

The repository intentionally contains only rendered host packages and their catalogs. Gluxer’s server, internal documents, and secrets do not ship here.

## Update

Refresh the installed Codex package with one command:

`codex plugin marketplace upgrade gluxer && codex plugin add gluxer@gluxer`
