# Gleam Claude Code plugins

A Claude Code [plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces) for Gleam.

## Install

```
/plugin marketplace add gleamdev/claude-plugins
/plugin install gleam@gleam
```

The `gleam` plugin bundles:

- **Gleam MCP server** — query coding-agent activity, telemetry, and audit data (tools: `query_activity`, `get_activity`).
- **Skills** — Gleam workflow skills (see [`plugins/gleam/skills/`](plugins/gleam/skills/)).

## Configuration

Set a Gleam API key (created in the Gleam web UI) before using the MCP server:

```bash
export GLEAM_API_KEY=glm_...
```

## Layout

```
.claude-plugin/marketplace.json   # marketplace manifest
plugins/gleam/
├── .claude-plugin/plugin.json    # plugin manifest
├── .mcp.json                     # remote Gleam MCP server (HTTP)
└── skills/                       # drop SKILL.md directories here
```

## Adding a skill

Create `plugins/gleam/skills/<skill-name>/SKILL.md` — see [`plugins/gleam/skills/README.md`](plugins/gleam/skills/README.md). No manifest changes needed; skills in that directory are auto-discovered.
