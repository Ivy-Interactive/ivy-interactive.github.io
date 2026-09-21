# Ivy Tendril Developer Portal

> Everything you need to integrate, orchestrate, and build on Ivy Tendril's agentic software factory.

## Quickstart & Local Setup

### 1. Model Context Protocol (MCP)
- Stdio transport: `tendril mcp`
- Streamable HTTP: `http://127.0.0.1:5010/mcp`
- MCP Manifest: [mcp.json](https://ivy-interactive.github.io/Ivy-Tendril-V2/.well-known/mcp.json)
- MCP Documentation: [MCP Guide](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/advanced/mcp)

### 2. Tendril CLI
```bash
tendril run             # Start background daemon on 127.0.0.1:5010
tendril plan create "Add OAuth2 PKCE flow"
tendril plan run <plan-id> --agent claude-code
tendril doctor          # Check environment health
```

## Self-Serve API Keys & Authentication
- 100% Free and Source-Available under FSL-1.1-ALv2.
- Local encrypted vault:
  ```bash
  tendril vault init
  tendril config set-key anthropic <your-key>
  tendril config set-key openai <your-key>
  ```
- OAuth 2.0 discovery: [oauth-authorization-server](https://ivy-interactive.github.io/Ivy-Tendril-V2/.well-known/oauth-authorization-server)

## Sandbox & Test Environment
```bash
tendril run --sandbox
curl -s http://127.0.0.1:5010/sandbox/plans
```

## Key Endpoints & Specifications
- OpenAPI 3.1.0: [openapi.json](https://ivy-interactive.github.io/Ivy-Tendril-V2/openapi.json)
- LLM Guidelines: [llms.txt](https://ivy-interactive.github.io/Ivy-Tendril-V2/llms.txt)
- Full Documentation: [llms-full.txt](https://ivy-interactive.github.io/Ivy-Tendril-V2/llms-full.txt)
- Sitemap: [sitemap.xml](https://ivy-interactive.github.io/Ivy-Tendril-V2/sitemap.xml)
- Getting Started: [Setup Guide](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/gettingstarted/introduction)
