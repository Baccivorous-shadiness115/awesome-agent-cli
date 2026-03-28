# Awesome Agent CLI

> A curated collection of CLI tools designed for AI agents — classified by domain, with tags, install commands, and auto-updating star counts.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/shuyhere/awesome-agent-cli/pulls)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## What is an "Agent CLI"?

An **Agent CLI** is a command-line tool specifically designed (or well-suited) for use by AI agents. Key characteristics:

- **Structured output** — JSON/NDJSON responses parseable by LLMs
- **Headless auth** — OAuth device flow or token-based auth (no browser required)
- **Dry-run support** — Preview destructive operations before execution
- **Auto-pagination** — Stream large datasets without manual page management
- **Discovery-driven** — Auto-generated commands from API specs

## Table of Contents

- [Workspace and Productivity Suites](#workspace-and-productivity-suites)
- [Meta-CLIs and Universal Hubs](#meta-clis-and-universal-hubs)
- [Research and Academic](#research-and-academic)
- [Developer Tools](#developer-tools)
- [Social and Networking](#social-and-networking)
- [Communication and Email](#communication-and-email)
- [Smart Home and IoT](#smart-home-and-iot)
- [Knowledge and Memory](#knowledge-and-memory)
- [Coding Agents](#coding-agents)
- [Agent Infrastructure](#agent-infrastructure)
- [Design Patterns](#design-patterns-across-agent-clis)
- [Tags Reference](#tags-reference)
- [Contributing](#contributing)

---

## Workspace and Productivity Suites

Full SaaS platform CLIs with broad API coverage.

| CLI | Stars | Install | Lang | Tags |
|-----|-------|---------|------|------|
| [**gws** (Google Workspace)](https://github.com/googleworkspace/cli) | ![Stars](https://img.shields.io/github/stars/googleworkspace/cli?style=flat&label=) | `npm i -g @googleworkspace/cli` | Rust | `productivity` `email` `calendar` `docs` `sheets` `drive` `chat` |
| [**lark-cli** (Feishu/Lark)](https://github.com/larksuite/cli) | ![Stars](https://img.shields.io/github/stars/larksuite/cli?style=flat&label=) | `npm i -g @larksuite/cli` | Go | `productivity` `messenger` `docs` `sheets` `calendar` `mail` `tasks` `meetings` `china` |
| [**dws** (DingTalk Workspace)](https://github.com/DingTalk-Real-AI/dingtalk-workspace-cli) | ![Stars](https://img.shields.io/github/stars/DingTalk-Real-AI/dingtalk-workspace-cli?style=flat&label=) | `curl -fsSL .../install.sh \| sh` | Go | `productivity` `contacts` `calendar` `todo` `attendance` `chat` `china` `mcp` |

### Details

**gws** — The gold standard. Dynamically generates its entire command surface from Google's Discovery Service — when Google adds an API, gws picks it up automatically. Ships 100+ agent skills, helper commands (e.g. `gws gmail +send`, `gws calendar +agenda`), and OpenClaw-compatible skill bundles. Supports three auth flows: interactive OAuth, service account, and pre-obtained token.

**lark-cli** — Official Feishu/Lark CLI from ByteDance. Three-layer architecture: shortcut commands (human+AI friendly), API commands (platform-synced), raw API (full coverage, 2500+ endpoints). Includes `--dry-run`, structured JSON, and identity switching (`--as user` / `--as bot`).

**dws** — Official DingTalk CLI. Uses a discovery-driven MCP (Model Context Protocol) JSON-RPC pipeline — doesn't hardcode commands, builds them from a market registry. Currently in co-creation phase (whitelist required).

---

## Meta-CLIs and Universal Hubs

Tools that wrap multiple services or turn arbitrary interfaces into CLIs.

| CLI | Stars | Install | Lang | Tags |
|-----|-------|---------|------|------|
| [**OpenCLI**](https://github.com/jackwener/opencli) | ![Stars](https://img.shields.io/github/stars/jackwener/opencli?style=flat&label=) | `npm i -g @jackwener/opencli` | TypeScript | `meta-cli` `browser` `scraping` `social-media` `electron` `hub` |
| [**x-cmd**](https://github.com/x-cmd/x-cmd) | ![Stars](https://img.shields.io/github/stars/x-cmd/x-cmd?style=flat&label=) | `eval "$(curl https://get.x-cmd.com)"` | Awk | `meta-cli` `package-manager` `1000+-tools` `agent-bootstrap` |

### Details

**OpenCLI** — Turns any website, Electron app, or local CLI into a unified CLI. 65+ site adapters (Bilibili, Twitter/X, Reddit, Xiaohongshu, YouTube, etc.) using Chrome's logged-in session. Also wraps desktop Electron apps (Cursor, ChatGPT, Notion, Discord) via CDP. Zero LLM cost at runtime — deterministic, same command = same output. Acts as a passthrough hub for `gh`, `gws`, `docker` with auto-install.

**x-cmd** — Bootstrap 1000+ CLI tools in seconds. Package manager + 100+ functional modules. Provides `llms.txt` manifest for agent discovery. No-sudo, pure awk core engine under 1MB.

---

## Research and Academic

Tools for academic workflows: papers, LaTeX, literature, publishing.

| CLI | Stars | Install | Lang | Tags |
|-----|-------|---------|------|------|
| [**olcli** (Overleaf CLI)](https://github.com/aloth/olcli) | ![Stars](https://img.shields.io/github/stars/aloth/olcli?style=flat&label=) | `npm i -g @aloth/olcli` | TypeScript | `research` `latex` `overleaf` `papers` `arxiv` `collaboration` |

### Details

**olcli** — Sync Overleaf LaTeX projects from the command line. Pull projects locally, push changes back, compile PDFs, download `.bbl` files for arXiv submissions. Essential for academic workflows where you need agent-driven paper writing without touching the Overleaf web UI.

---

## Developer Tools

Code hosting, CI/CD, version control, and dev infrastructure.

| CLI | Stars | Install | Lang | Tags |
|-----|-------|---------|------|------|
| [**gh** (GitHub CLI)](https://github.com/cli/cli) | ![Stars](https://img.shields.io/github/stars/cli/cli?style=flat&label=) | `brew install gh` | Go | `developer` `github` `issues` `prs` `ci` `code-review` `api` |

### Details

**gh** — The de facto standard developer CLI. Issues, PRs, CI runs, code review, API queries. Massive ecosystem of extensions. Every AI coding agent supports it natively.

---

## Social and Networking

CLIs for social platforms and professional networking.

| CLI | Stars | Install | Lang | Tags |
|-----|-------|---------|------|------|
| [**linkedin-cli**](https://github.com/Linked-API/linkedin-cli) | ![Stars](https://img.shields.io/github/stars/Linked-API/linkedin-cli?style=flat&label=) | `npm i -g @linkedapi/linkedin-cli` | TypeScript | `social` `networking` `linkedin` `profiles` `messaging` `job-search` |
| [**OpenCLI adapters**](https://github.com/jackwener/opencli) | ![Stars](https://img.shields.io/github/stars/jackwener/opencli?style=flat&label=) | See OpenCLI above | TypeScript | `social` `twitter` `reddit` `bilibili` `xiaohongshu` `youtube` |

### Details

**linkedin-cli** — Cloud-browser-based LinkedIn automation. Fetch profiles, search people/companies, send messages, manage connections, create posts, react, comment. Anti-detection built in (residential IPs, human-like patterns). Structured JSON output. Multi-account support. Requires [Linked API](https://linkedapi.io) account.

---

## Communication and Email

Messaging, email, and chat CLIs.

| CLI | Stars | Install | Lang | Tags |
|-----|-------|---------|------|------|
| [**himalaya**](https://github.com/pimalaya/himalaya) | ![Stars](https://img.shields.io/github/stars/pimalaya/himalaya?style=flat&label=) | `brew install himalaya` | Rust | `email` `imap` `smtp` `multi-account` `mml` |
| [**gws gmail**](https://github.com/googleworkspace/cli) | ![Stars](https://img.shields.io/github/stars/googleworkspace/cli?style=flat&label=) | See gws above | Rust | `email` `gmail` `google` |
| [**lark-cli im**](https://github.com/larksuite/cli) | ![Stars](https://img.shields.io/github/stars/larksuite/cli?style=flat&label=) | See lark-cli above | Go | `messaging` `feishu` `lark` `china` |

### Details

**himalaya** — Multi-account IMAP/SMTP email client for the terminal. Compose with MML (MIME Meta Language). List, read, write, reply, forward, search, and organize emails from CLI. Privacy-first, local-only.

---

## Smart Home and IoT

Control physical devices from the command line.

| CLI | Stars | Install | Lang | Tags |
|-----|-------|---------|------|------|
| [**openhue**](https://github.com/openhue/openhue-cli) | ![Stars](https://img.shields.io/github/stars/openhue/openhue-cli?style=flat&label=) | `brew install openhue` | Go | `smart-home` `lights` `hue` `scenes` `iot` |

---

## Knowledge and Memory

Persistent context, knowledge management, and agent memory.

| CLI | Stars | Install | Lang | Tags |
|-----|-------|---------|------|------|
| [**OpenContext**](https://github.com/0xranx/OpenContext) | ![Stars](https://img.shields.io/github/stars/0xranx/OpenContext?style=flat&label=) | `npm i -g @aicontextlab/cli` | TypeScript | `knowledge` `memory` `context` `persistence` `cross-repo` `mcp` |

### Details

**OpenContext** — Personal context store for AI agents. Persistent memory across repos/sessions. Ships CLI + MCP server + Desktop GUI + Web UI. "Load history first, then act; ship, then persist." Skills and slash commands for Cursor, Claude Code, and Codex. Brings your own coding agent — no extra subscription.

---

## Coding Agents

Terminal-based AI coding assistants that act as CLI tools themselves.

| CLI | Stars | Install | Lang | Tags |
|-----|-------|---------|------|------|
| [**oh-my-pi**](https://github.com/can1357/oh-my-pi) | ![Stars](https://img.shields.io/github/stars/can1357/oh-my-pi?style=flat&label=) | `npm i -g @oh-my-pi/pi-coding-agent` | TypeScript | `coding-agent` `lsp` `python` `browser` `subagents` `skills` |
| [**Claude Code**](https://github.com/anthropics/claude-code) | ![Stars](https://img.shields.io/github/stars/anthropics/claude-code?style=flat&label=) | `npm i -g @anthropic-ai/claude-code` | TypeScript | `coding-agent` `anthropic` `terminal` `ai` |
| [**Codex** (OpenAI)](https://github.com/openai/codex) | ![Stars](https://img.shields.io/github/stars/openai/codex?style=flat&label=) | `npm i -g @openai/codex` | TypeScript | `coding-agent` `openai` `terminal` `ai` |
| [**Gemini CLI**](https://github.com/google/gemini-cli) | ![Stars](https://img.shields.io/github/stars/google/gemini-cli?style=flat&label=) | `npm i -g @google/gemini-cli` | TypeScript | `coding-agent` `google` `terminal` `ai` |

### Details

**oh-my-pi** — Feature-rich coding agent with hash-anchored edits, LSP integration (40+ languages), persistent Python IPython kernel, browser tools, subagents, TTSR (zero-context-use rules that only inject when needed), agentic git commits, and custom skills/hooks.

---

## Agent Infrastructure

Runtimes, orchestrators, and platforms that host or coordinate agents.

| Tool | Stars | Install | Tags |
|------|-------|---------|------|
| [**OpenClaw**](https://github.com/openclaw/openclaw) | ![Stars](https://img.shields.io/github/stars/openclaw/openclaw?style=flat&label=) | `npm i -g openclaw` | `agent-runtime` `orchestrator` `skills` `multi-channel` `discord` `telegram` `whatsapp` |
| [**Forge**](https://github.com/initializ/forge) | ![Stars](https://img.shields.io/github/stars/initializ/forge?style=flat&label=) | — | `agent-runtime` `enterprise` `containerized` `secure` |
| [**refly**](https://github.com/refly-ai/refly) | ![Stars](https://img.shields.io/github/stars/refly-ai/refly?style=flat&label=) | — | `skills-builder` `workflow` `multi-agent` |

---

## Design Patterns Across Agent CLIs

Common architectural patterns observed across agent-native CLIs:

| Pattern | Description | Examples |
|---------|-------------|----------|
| Structured JSON Output | Every response is parseable JSON/NDJSON | All workspace CLIs |
| `--dry-run` | Preview destructive operations | gws, lark-cli, dws |
| Three-Layer Architecture | Shortcuts, API commands, Raw API | lark-cli, dws |
| Bundled Skills | SKILL.md files with `npx skills add` | gws, lark-cli, dws |
| OAuth Device Flow | Headless auth for agents | gws, lark-cli |
| Auto-Pagination | `--page-all` with NDJSON streaming | gws, lark-cli |
| Discovery-Driven | Commands built from API specs at runtime | gws, dws |
| Output Formats | `--format json\|table\|csv\|yaml\|ndjson` | Most CLIs |
| Identity Switching | `--as user` / `--as bot` | lark-cli |
| Encrypted Credential Storage | OS keyring or AES-256-GCM at rest | gws, dws |

---

## Tags Reference

| Tag | Meaning |
|-----|---------|
| `productivity` | Workspace / office suite |
| `research` | Academic / scientific workflows |
| `developer` | Code, CI/CD, version control |
| `social` | Social media platforms |
| `networking` | Professional networking |
| `email` | Email management |
| `messaging` | Chat / instant messaging |
| `smart-home` | IoT / home automation |
| `knowledge` | Knowledge management / memory |
| `coding-agent` | AI coding assistant |
| `agent-runtime` | Agent hosting / orchestration |
| `meta-cli` | Wraps multiple tools/services |
| `china` | Primarily serves Chinese market |
| `mcp` | Uses Model Context Protocol |
| `hub` | Aggregates other CLIs |
| `skills-builder` | Creates/manages agent skills |

---

## Contributing

Found a CLI that should be listed here? PRs welcome.

### Criteria for inclusion

1. **CLI-first** — must be usable from the command line
2. **Agent-friendly** — structured output (JSON), or bundled agent skills, or designed for programmatic use
3. **Maintained** — actively maintained (commits in last 6 months)
4. **Open source** or has a free tier

### How to contribute

1. Fork this repo
2. Add your CLI to the appropriate category table
3. Include: name, repo link, install command, language, tags
4. Submit a PR with a brief description of why it qualifies

---

## License

[MIT](LICENSE)

---

*Curated by [@shuyhere](https://github.com/shuyhere) — built with the help of AI agents, for AI agents.*
