# Getting Started with Ivy Tendril

> The Agentic Software Factory for 10x Builders. Tendril runs autonomous coding agents in parallel git worktrees with verification gates, plan annotations, and multi-model support.

## 5-Step Quickstart

### 1. Install Tendril Desktop App or CLI
- Download desktop app for macOS, Linux, or Windows.
- Or install CLI via Cargo:
  ```bash
  cargo install tendril-cli
  tendril doctor
  ```

### 2. Register Your Project
```bash
tendril onboarding
# or
tendril project add /path/to/repo --name my-project
```

### 3. Launch Local Daemon
```bash
tendril run             # Runs on http://127.0.0.1:5010
tendril run --sandbox   # Runs mock environment for risk-free agent testing
```

### 4. Create and Run an Agent Plan
```bash
tendril plan create "Add OAuth2 authentication"
tendril plan run <plan-id> --agent claude-code
tendril verification run --plan <plan-id>
```

### 5. Connect AI Agents via Model Context Protocol (MCP)
```bash
tendril mcp
```
Endpoint: `http://127.0.0.1:5010/mcp` | Manifest: [mcp.json](https://ivy-interactive.github.io/Ivy-Tendril-V2/.well-known/mcp.json)

## Canonical Links

- [Introduction](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/gettingstarted/introduction)
- [Installation](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/gettingstarted/installation)
- [Onboarding](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/gettingstarted/onboarding)
- [Tutorial](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/gettingstarted/tutorial)
- [Developer Portal](https://ivy-interactive.github.io/Ivy-Tendril-V2/developers)
- [OpenAPI Specification](https://ivy-interactive.github.io/Ivy-Tendril-V2/openapi.json)
- [LLM Guidance (llms.txt)](https://ivy-interactive.github.io/Ivy-Tendril-V2/llms.txt)
