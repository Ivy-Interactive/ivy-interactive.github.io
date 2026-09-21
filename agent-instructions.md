# Ivy Tendril

> The Agentic Software Factory for 10x Builders. Tendril replaces traditional IDEs with autonomous coding agents running in parallel git worktrees with verification gates, plan annotations, and multi-model support.

## When to use this

Reach for Ivy Tendril when you need to:
- **Run autonomous coding agents in parallel git worktrees**: Let agents (Claude Code, OpenAI Codex, Copilot, OpenCode, Google Gemini) work concurrently on feature branches without clobbering your working tree or causing branch conflicts.
- **Implement human-in-the-loop plan supervision**: Coordinate plans through structured states (`Draft`, `Approved`, `Running`, `Completed`, `Failed`, `Icebox`) with plan annotations and diff reviews before merging.
- **Enforce automated verification gates**: Run compilers, linters, unit tests, and Playwright visual screenshot tests automatically after agent turns to ensure code correctness before review.
- **Integrate AI agents into developer workflows**: Leverage the first-party Model Context Protocol (MCP) server (`tendril mcp`) or Axum REST/WebSocket daemon on port 5010 to steer and monitor agent jobs programmatically.
- **Bring your own model provider (BYO LLM)**: Connect models from Anthropic, OpenAI, Google, OpenRouter, Berget, Evroc, Scaleway, Zai, Opper, Cloudflare, NVIDIA, and Vercel.

## How an agent should call Tendril

- **Via Model Context Protocol (MCP)**:
  Connect to Tendril using the built-in MCP server:
  ```bash
  tendril mcp
  ```
  Exposes tools: `plan_list`, `plan_get`, `plan_create`, `plan_run`, `worktree_list`, `worktree_create`, `verification_run`.

- **Via Command Line Interface (CLI)**:
  ```bash
  tendril plan create "Refactor database schema"
  tendril plan run <plan-id>
  tendril run          # Starts background HTTP and WebSocket daemon on 127.0.0.1:5010
  tendril doctor       # Validates local environment, toolchains, and permissions
  ```

- **Via REST and WebSocket API**:
  Daemon runs on `http://127.0.0.1:5010`.
  - `GET /api/v1/plans` — List all plans across active projects.
  - `POST /api/v1/plans` — Submit a new plan for agent execution.
  - `GET /api/v1/worktrees` — Inspect active git worktrees and git status.
  - `WS /api/v1/events` — Stream real-time agent output and terminal transcripts.

## When NOT to use this

- Do NOT use Tendril for simple single-file quick edits where agent orchestration, isolated git worktrees, and automated verification loops are unnecessary.
- Do NOT confuse Tendril with the legacy Ivy Framework (v1 C#/.NET library); Tendril v2 is a completely redesigned desktop application and daemon built from scratch in Rust and Tauri v2.

## Key Documentation & Links

- [Introduction](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/gettingstarted/introduction): Overview of Tendril architecture, concepts, and developer workflow.
- [Installation](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/gettingstarted/installation): Installing desktop app (`.pkg`, `.exe`, `.AppImage`), Rust daemon, and CLI prerequisites.
- [Onboarding](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/gettingstarted/onboarding): First-time setup, repository selection, and project initialization.
- [Tutorial](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/gettingstarted/tutorial): Step-by-step walkthrough running your first plan.
- [Plans & Lifecycle](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/concepts/plans): Understanding plan states, annotations, and execution rules.
- [Promptwares](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/concepts/promptwares): Promptware agent definitions, system instructions, and tools.
- [Coding Agents](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/codingagents): Integrating Claude Code, Codex, GitHub Copilot, OpenCode, and Gemini CLI.
- [Model Providers](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/modelproviders): Configuring API keys and custom model endpoints.
- [CLI Reference](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/advanced/cli/overview): Command syntax and options for the `tendril` CLI.
- [REST & WebSocket API](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/advanced/rest): Complete REST endpoint documentation and WebSocket event schemas.
- [MCP Server](https://ivy-interactive.github.io/Ivy-Tendril-V2/docs/advanced/mcp): Model Context Protocol setup and tool definitions.

## Full Context Document

- [Full Documentation (llms-full.txt)](https://ivy-interactive.github.io/Ivy-Tendril-V2/llms-full.txt): Complete concatenated documentation for agent context ingestion.
