# Adaptive Gears Plugin

Claude Code plugin for canonical patterns in AWS, infrastructure, Python, and data engineering.

## Install

```
/plugin marketplace add https://github.com/adaptivegears/adaptivegears-plugin
/plugin install adaptivegears
```

## Commands

| Command | Description |
|---------|-------------|
| `/adaptivegears-enable` | Activate companion mode - proactive pattern matching |
| `/adaptivegears-maintainer` | Activate maintainer mode - companion + gap detection |
| `/adaptivegears-disable` | Return to passive mode (default) |

## Modes

### Disabled (default)

KB tools available but passive. Only used when explicitly requested.

### Enabled (companion mode)

- Proactively searches KB before implementing AWS/infra/Python tasks
- Follows patterns found as the canonical approach
- Aligns code style with KB solutions

### Maintainer

Everything from companion mode, plus:

- Identifies documentation gaps during work
- Suggests new content for the KB
- Helps grow and curate the knowledge base

## MCP Server

Plugin bundles connection to `https://mcp.adaptivegears.studio/mcp`.

Tools available:

| Tool | Description |
|------|-------------|
| `search(query, limit)` | Semantic search across KB |
| `read(category, doc, anchor)` | Read markdown content |
