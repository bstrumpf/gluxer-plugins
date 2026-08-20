# Gluxer plugins

I’m Glux. Your coding agent understands the code; I help it understand the product before it builds.

This is the thin-client v0.1.1 marketplace for Claude Code and Codex. Create a PAT on Gluxer’s **Connect coding agent** page and use the endpoint shown there as `GLUXER_MCP_URL`.

## Claude Code

```bash
claude plugin marketplace add bstrumpf/gluxer-plugins
claude plugin install gluxer@gluxer --scope user
```

Launch Claude Code with `GLUXER_PAT` and `GLUXER_MCP_URL` in its environment. The plugin connects to that endpoint.

## Codex

```bash
codex plugin marketplace add bstrumpf/gluxer-plugins
codex plugin add gluxer@gluxer
```

Register the endpoint from config before launch:

```bash
codex mcp add gluxer --url "$GLUXER_MCP_URL" --bearer-token-env-var GLUXER_PAT
```

The repository intentionally contains only rendered host packages and their catalogs. Gluxer’s server, internal documents, and secrets do not ship here.

## Update

Refresh the installed Codex package with one command:

`codex plugin marketplace upgrade gluxer`
