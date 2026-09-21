# Ivy Tendril Model Context Protocol (MCP) Server

> Connect AI coding agents directly to Tendril's autonomous plan lifecycle and git worktree engine.

## Connection

### Stdio
```bash
tendril mcp
```

### Streamable HTTP
- Endpoint: `http://127.0.0.1:5010/mcp`
- Manifest: [mcp.json](https://ivy-interactive.github.io/Ivy-Tendril-V2/.well-known/mcp.json)

## Configuration
```json
{
  "mcpServers": {
    "tendril": {
      "command": "tendril",
      "args": ["mcp"]
    }
  }
}
```

## Available Tools
- `plan_list`: List plans in workspace filtered by status
- `plan_get`: Retrieve plan details, annotations, and verification status
- `plan_create`: Create new plan for autonomous coding agent
- `plan_run`: Trigger approved plan in isolated git worktree
- `worktree_list`: List active isolated git worktrees
- `verification_run`: Run verification test suites (compiler, linter, tests, visual)

## Links
- [Complete MCP Documentation](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/advanced/mcp)
- [Developer Portal](https://ivy-interactive.github.io/Ivy-Tendril-V2/developers)
- [OpenAPI Specification](https://ivy-interactive.github.io/Ivy-Tendril-V2/openapi.json)
