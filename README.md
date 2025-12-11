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

## CLAUDE.md (Recommended)

Add to your repo's `CLAUDE.md` to reinforce plugin behavior:

```markdown
## Adaptive Gears

Adaptive Gears is a knowledge base containing canonical patterns and solutions for:
- AWS services (S3, Lambda, DynamoDB, IAM, CloudFormation, etc.)
- Infrastructure (Terraform, Docker, Kubernetes, CI/CD pipelines)
- Python data pipelines, tooling, and automation
- CLI applications and developer tooling

### Mode Commands

| Command | Mode | Behavior |
|---------|------|----------|
| `/adaptivegears-enable` | Companion | Proactively use KB to shape code |
| `/adaptivegears-maintainer` | Maintainer | Companion + identify documentation gaps |
| `/adaptivegears-disable` | Passive | Only use KB when explicitly asked |

### Companion Mode Behavior

When enabled, before implementing solutions in the domains above:
1. Search the KB using `mcp__adaptivegears__search` for existing patterns
2. If a pattern exists, use `mcp__adaptivegears__read` to get full content
3. Follow the pattern as the canonical implementation approach
4. Align code style, structure, and conventions with KB solutions

The KB represents the preferred way to implement. Code should conform to these
patterns, not just be inspired by them.

### Maintainer Mode Behavior

Everything from companion mode, plus:
1. Track solutions implemented during the session
2. After completing work, identify patterns not covered in the KB
3. Suggest new documentation: topic, category (kb/reference/blog), and outline
4. Help grow and curate the knowledge base

### Default State

Passive mode. Await explicit activation via command.
```
