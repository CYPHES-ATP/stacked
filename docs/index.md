<div align="center">

# CYPHES

<img src="../public/cyphes-mark.svg?v=cyphes-node" alt="CYPHES mark" width="180" />

CYPHES is a local autonomous coding-agent node for the CYPHES Agent Transfer Protocol. It is built for visible approvals, tool execution, model-provider control, and receipt-backed work.

**Version:** 0.1.4 Phase 1 node · **License:** GPL-3.0 · [GitHub](https://github.com/CYPHES-ATP/node)

</div>

---

## What CYPHES Does

You give CYPHES a task in natural language. It plans, reads and writes files, runs shell commands, searches the web, and iterates inside your terminal with every step visible in real time.

```bash
cyphes "add input validation to the signup form"
```

CYPHES reads your codebase, implements changes across multiple files, runs tests, and reports back without requiring you to leave the terminal.

---

## Network Role

CYPHES Node is the first local execution node for ATP. Phase 1 focuses on a trustworthy local runtime and branded control surface. Later phases add explicit agent transfer, independent review, synthesis, and durable receipts.

---

## Key Capabilities

### Agentic Loop
CYPHES runs a multi-turn loop: it streams a response from the model, executes tool calls, feeds results back into the session, and continues until the task is done or the turn limit is reached.

### Built-In Tools
- **File operations** — read, write, edit, patch, batch-edit
- **Shell** — bash with persistent working directory and environment
- **Search** — glob file patterns, grep contents, web search, web fetch
- **Git** — commit, branch, worktree
- **Notebooks** — read and edit Jupyter notebooks
- **Desktop automation** — screenshot, click, type
- **Task management** — create, track, and complete tasks

### LLM Providers
Anthropic Claude, OpenAI, Google Gemini, AWS Bedrock, Azure OpenAI, Ollama, Groq, Mistral, DeepSeek, xAI, Cohere, OpenRouter, Together AI, Perplexity, GitHub Copilot, Cerebras, LM Studio, and LLaMA.cpp.

### CYPHES Terminal UI
A ratatui-based TUI with real-time streaming, syntax-highlighted code blocks, diff viewer, permission dialogs, slash command autocomplete, session browser, and keybinding controls.

### Agent Transfer Path
Phase 1 keeps work local. The runtime is being shaped around ATP concepts: contracts, approvals, receipts, provider identity, artifact hashes, review findings, and final settlement records.

---

## Quick Start

**1. Build locally**

```bash
git clone https://github.com/CYPHES-ATP/node
cd node/src-rust
cargo run -p cyphes -- --print "explain this repo"
```

**2. Set your provider key**

```bash
export ANTHROPIC_API_KEY=sk-ant-...
```

**3. Run interactively**

```bash
cargo run -p cyphes
```

After installation/release packaging is audited, the intended command is:

```bash
cyphes
```

---

## Configuration

The runtime reads `~/.cyphes/settings.json` at startup. Common settings:

```json
{
  "config": {
    "model": "claude-opus-4-6",
    "permission_mode": "default",
    "auto_compact": true,
    "compact_threshold": 0.8
  }
}
```

See [Configuration](configuration) for the full reference.

---

## Interactive Vs Headless

| Mode | Command | Use case |
|------|---------|----------|
| Interactive TUI | `cargo run -p cyphes` | Day-to-day local testing |
| Installed TUI | `cyphes` | Day-to-day coding after packaging |
| Single prompt | `cyphes "task"` | Quick one-shot tasks |
| Headless print | `cyphes --print "task"` | Scripts, CI |
| JSON output | `cyphes --output-format json "task"` | Machine consumption |
| Stream JSON | `cyphes --output-format stream-json "task"` | Real-time piping |

---

## Next Steps

- [Installation](installation) — build from source and package locally
- [Authentication](auth) — API keys and OAuth
- [Configuration](configuration) — settings reference
- [Slash Commands](commands) — command reference
- [Tools Reference](tools) — tools and permission levels
- [Providers](providers) — configuring each LLM provider
- [MCP Integration](mcp) — Model Context Protocol servers
- [Plugins](plugins) — building and using plugins
- [Agents](agents) — orchestration foundations
- [Hooks](hooks) — event-driven automation
- [Advanced Features](advanced) — extended thinking, sessions, and more
