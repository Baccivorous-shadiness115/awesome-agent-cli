# 🤖 Awesome Agent CLI

> A curated collection of CLI tools designed for AI agents — classified by domain, with tags, install commands, and agent-readiness ratings.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/shuyhere/awesome-agent-cli/pulls)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## What is an "Agent CLI"?

An **Agent CLI** is a command-line tool specifically designed (or well-suited) for use by AI agents. Key characteristics:

- 📊 **Structured output** — JSON/NDJSON responses parseable by LLMs
- 🧠 **Agent Skills** — Bundled SKILL.md files that teach agents how to use the tool
- 🔐 **Headless auth** — OAuth device flow or token-based auth (no browser required)
- 📄 **Dry-run support** — Preview destructive operations before execution
- 📑 **Auto-pagination** — Stream large datasets without manual page management
- 🔍 **Discovery-driven** — Auto-generated commands from API specs

## Table of Contents

- [Workspace & Productivity Suites](#-workspace--productivity-suites)
- [Meta-CLIs & Universal Hubs](#-meta-clis--universal-hubs)
- [Research & Academic](#-research--academic)
- [Developer Tools](#-developer-tools)
- [Social & Networking](#-social--networking)
- [Communication & Email](#-communication--email)
- [Smart Home & IoT](#-smart-home--iot)
- [Knowledge & Memory](#-knowledge--memory)
- [Coding Agents](#-coding-agents)
- [Agent Infrastructure](#-agent-infrastructure)
- [Skills Ecosystem](#-skills-ecosystem)
- [Design Patterns](#design-patterns-across-agent-clis)
- [Contributing](#contributing)

---

## 🏢 Workspace & Productivity Suites

Full SaaS platform CLIs with broad API coverage.

| CLI | Repo | Stars | Install | Lang | Agent Skills | Tags |
|-----|------|-------|---------|------|-------------|------|
| **gws** (Google Workspace) | [googleworkspace/cli](https://github.com/googleworkspace/cli) | ⭐ 22.8k | `npm i -g @googleworkspace/cli` | Rust | ✅ 100+ skills | `productivity` `email` `calendar` `docs` `sheets` `drive` `chat` |
| **lark-cli** (Feishu/Lark) | [larksuite/cli](https://github.com/larksuite/cli) | ⭐ 501 | `npm i -g @larksuite/cli` | Go | ✅ 19 skills | `productivity` `messenger` `docs` `sheets` `calendar` `mail` `tasks` `meetings` `china` |
| **dws** (DingTalk Workspace) | [DingTalk-Real-AI/dingtalk-workspace-cli](https://github.com/DingTalk-Real-AI/dingtalk-workspace-cli) | ⭐ 701 | `curl -fsSL .../install.sh \| sh` | Go | ✅ Per-product skills | `productivity` `contacts` `calendar` `todo` `attendance` `chat` `china` `mcp` |

### Key Details

**gws** — The gold standard. Dynamically generates its entire command surface from Google's Discovery Service — when Google adds an API, gws picks it up automatically. Ships 100+ agent skills, helper commands (e.g. `gws gmail +send`, `gws calendar +agenda`), and OpenClaw-compatible skill bundles. Supports three auth flows: interactive OAuth, service account, and pre-obtained token.

**lark-cli** — Official Feishu/Lark CLI from ByteDance. Three-layer architecture: shortcut commands (human+AI friendly) → API commands (platform-synced) → raw API (full coverage, 2500+ endpoints). Includes `--dry-run`, structured JSON, and identity switching (`--as user` / `--as bot`).

**dws** — Official DingTalk CLI. Uses a discovery-driven MCP (Model Context Protocol) JSON-RPC pipeline — doesn't hardcode commands, builds them from a market registry. Currently in co-creation phase (whitelist required).

---

## 🌐 Meta-CLIs & Universal Hubs

Tools that wrap multiple services or turn arbitrary interfaces into CLIs.

| CLI | Repo | Stars | Install | Lang | Tags |
|-----|------|-------|---------|------|------|
| **OpenCLI** | [jackwener/opencli](https://github.com/jackwener/opencli) | ⭐ 8.2k | `npm i -g @jackwener/opencli` | TypeScript | `meta-cli` `browser` `scraping` `social-media` `electron` `hub` |
| **x-cmd** | [x-cmd/x-cmd](https://github.com/x-cmd/x-cmd) | ⭐ 4.2k | `eval "$(curl https://get.x-cmd.com)"` | Awk | `meta-cli` `package-manager` `1000+-tools` `agent-bootstrap` |

### Key Details

**OpenCLI** — Turns ANY website, Electron app, or local CLI into a unified CLI. 65+ site adapters (Bilibili, Twitter/X, Reddit, Xiaohongshu, YouTube, etc.) using Chrome's logged-in session. Also wraps desktop Electron apps (Cursor, ChatGPT, Notion, Discord) via CDP. Zero LLM cost at runtime — deterministic, same command = same output. Acts as a passthrough hub for `gh`, `gws`, `docker` with auto-install.

**x-cmd** — Bootstrap 1000+ CLI tools in seconds. Package manager + 100+ functional modules. Provides `llms.txt` manifest for agent discovery. No-sudo, pure awk core engine <1MB. Great for provisioning agent environments.

---

## 📚 Research & Academic

Tools for academic workflows: papers, LaTeX, literature, publishing.

| CLI | Repo | Stars | Install | Lang | Tags |
|-----|------|-------|---------|------|------|
| **olcli** (Overleaf CLI) | [aloth/olcli](https://github.com/aloth/olcli) | — | `npm i -g @aloth/olcli` | TypeScript | `research` `latex` `overleaf` `papers` `arxiv` `collaboration` |
| **arxiv-search** | Various | — | — | — | `research` `papers` `literature` `search` |

### Key Details

**olcli** — Sync Overleaf LaTeX projects from the command line. Pull projects locally, push changes back, compile PDFs, download `.bbl` files for arXiv submissions. Essential for academic workflows where you need agent-driven paper writing without touching the Overleaf web UI.

---

## 🛠️ Developer Tools

Code hosting, CI/CD, version control, and dev infrastructure.

| CLI | Repo | Stars | Install | Lang | Agent Skills | Tags |
|-----|------|-------|---------|------|-------------|------|
| **gh** (GitHub CLI) | [cli/cli](https://github.com/cli/cli) | ⭐ 48k+ | `brew install gh` | Go | ✅ Via extensions | `developer` `github` `issues` `prs` `ci` `code-review` `api` |
| **xurl** (X/Twitter API) | — | — | — | — | ✅ OpenClaw skill | `developer` `social-media` `twitter` `api` |

### Key Details

**gh** — The de facto standard developer CLI. Issues, PRs, CI runs, code review, API queries. Massive ecosystem of extensions. Every AI coding agent supports it natively.

---

## 👥 Social & Networking

CLIs for social platforms and professional networking.

| CLI | Repo | Stars | Install | Lang | Tags |
|-----|------|-------|---------|------|------|
| **linkedin-cli** | [Linked-API/linkedin-cli](https://github.com/Linked-API/linkedin-cli) | — | `npm i -g @linkedapi/linkedin-cli` | TypeScript | `social` `networking` `linkedin` `profiles` `messaging` `job-search` |
| **OpenCLI adapters** | [jackwener/opencli](https://github.com/jackwener/opencli) | ⭐ 8.2k | See OpenCLI above | TypeScript | `social` `twitter` `reddit` `bilibili` `xiaohongshu` `youtube` |

### Key Details

**linkedin-cli** — Cloud-browser-based LinkedIn automation. Fetch profiles, search people/companies, send messages, manage connections, create posts, react, comment. Anti-detection built in (residential IPs, human-like patterns). Structured JSON output. Multi-account support. Requires [Linked API](https://linkedapi.io) account.

---

## 📧 Communication & Email

Messaging, email, and chat CLIs.

| CLI | Repo | Stars | Install | Lang | Agent Skills | Tags |
|-----|------|-------|---------|------|-------------|------|
| **himalaya** | [pimalaya/himalaya](https://github.com/pimalaya/himalaya) | ⭐ 3k+ | `brew install himalaya` | Rust | ✅ OpenClaw skill | `email` `imap` `smtp` `multi-account` `mml` |
| **wacli** (WhatsApp CLI) | — | — | — | — | ✅ OpenClaw skill | `messaging` `whatsapp` `chat` |
| **gws gmail** | [googleworkspace/cli](https://github.com/googleworkspace/cli) | ⭐ 22.8k | See gws above | Rust | ✅ | `email` `gmail` `google` |
| **lark-cli im** | [larksuite/cli](https://github.com/larksuite/cli) | ⭐ 501 | See lark-cli above | Go | ✅ | `messaging` `feishu` `lark` `china` |

### Key Details

**himalaya** — Multi-account IMAP/SMTP email client for the terminal. Compose with MML (MIME Meta Language). List, read, write, reply, forward, search, and organize emails from CLI. Privacy-first, local-only.

---

## 🏠 Smart Home & IoT

Control physical devices from the command line.

| CLI | Repo | Stars | Install | Lang | Agent Skills | Tags |
|-----|------|-------|---------|------|-------------|------|
| **openhue** | [openhue/openhue-cli](https://github.com/openhue/openhue-cli) | — | `brew install openhue` | Go | ✅ OpenClaw skill | `smart-home` `lights` `hue` `scenes` `iot` |
| **sonoscli** | — | — | — | — | ✅ OpenClaw skill | `smart-home` `audio` `speakers` `sonos` `music` |

---

## 🧠 Knowledge & Memory

Persistent context, knowledge management, and agent memory.

| CLI | Repo | Stars | Install | Lang | Tags |
|-----|------|-------|---------|------|------|
| **OpenContext** | [0xranx/OpenContext](https://github.com/0xranx/OpenContext) | ⭐ 467 | `npm i -g @aicontextlab/cli` | TypeScript | `knowledge` `memory` `context` `persistence` `cross-repo` `mcp` |

### Key Details

**OpenContext** — Personal context store for AI agents. Persistent memory across repos/sessions. Ships CLI + MCP server + Desktop GUI + Web UI. "Load history first, then act; ship, then persist." Skills + slash commands for Cursor/Claude Code/Codex. Brings your own coding agent — no extra subscription.

---

## 🤖 Coding Agents

Terminal-based AI coding assistants that act as CLI tools themselves.

| CLI | Repo | Stars | Install | Lang | Tags |
|-----|------|-------|---------|------|------|
| **Claude Code** | [anthropics/claude-code](https://github.com/anthropics/claude-code) | — | `npm i -g @anthropic-ai/claude-code` | TypeScript | `coding-agent` `anthropic` `terminal` `ai` |
| **Codex** (OpenAI) | [openai/codex](https://github.com/openai/codex) | — | `npm i -g @openai/codex` | TypeScript | `coding-agent` `openai` `terminal` `ai` |
| **oh-my-pi** | [can1357/oh-my-pi](https://github.com/can1357/oh-my-pi) | ⭐ 2.4k | `npm i -g @oh-my-pi/pi-coding-agent` | TypeScript | `coding-agent` `lsp` `python` `browser` `subagents` `skills` |
| **OpenCode** | — | — | — | — | `coding-agent` `open-source` `terminal` `ai` |
| **Gemini CLI** | [google/gemini-cli](https://github.com/google/gemini-cli) | — | `npm i -g @google/gemini-cli` | TypeScript | `coding-agent` `google` `terminal` `ai` |

### Key Details

**oh-my-pi** — Feature-rich coding agent with hash-anchored edits, LSP integration (40+ languages), persistent Python IPython kernel, browser tools, subagents, TTSR (zero-context-use rules that only inject when needed), agentic git commits, and custom skills/hooks.

---

## ⚙️ Agent Infrastructure

Runtimes, orchestrators, and platforms that host or coordinate agents.

| Tool | Repo | Stars | Install | Tags |
|------|------|-------|---------|------|
| **OpenClaw** | [openclaw/openclaw](https://github.com/openclaw/openclaw) | — | `npm i -g openclaw` | `agent-runtime` `orchestrator` `skills` `multi-channel` `discord` `telegram` `whatsapp` |
| **Forge** (OpenClaw for Enterprise) | [initializ/forge](https://github.com/initializ/forge) | — | — | `agent-runtime` `enterprise` `containerized` `secure` |
| **ai-terminal** | [AiTerminalFoundation/ai-terminal](https://github.com/AiTerminalFoundation/ai-terminal) | — | — | `agent-runtime` `terminal` `ai-mate` |
| **refly** | [refly-ai/refly](https://github.com/refly-ai/refly) | — | — | `skills-builder` `workflow` `multi-agent` |

---

## 📦 Skills Ecosystem

Skill registries, curated lists, and the AgentSkills specification.

| Resource | Repo / URL | Description | Tags |
|----------|-----------|-------------|------|
| **AgentSkills Spec** | [agentskills/agentskills](https://github.com/agentskills/agentskills) | The specification and documentation for Agent Skills format | `spec` `standard` |
| **Anthropic Skills** | [anthropics/skills](https://github.com/anthropics/skills) | Official skills from Anthropic | `official` `claude` |
| **ClawHub** | [clawhub.ai](https://clawhub.ai) | OpenClaw skill registry — `npx clawhub install <skill>` | `registry` `openclaw` |
| **awesome-agent-skills** | [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | 1000+ skills from official dev teams and community | `curated-list` `multi-agent` |
| **awesome-openclaw-skills** | [VoltAgent/awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) | 5,400+ skills filtered and categorized from OpenClaw registry | `curated-list` `openclaw` |
| **antigravity-awesome-skills** | [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | 1,326+ installable skills with installer CLI | `curated-list` `installer` |
| **awesome-claude-code** | [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) | Skills, hooks, slash-commands, orchestrators for Claude Code | `curated-list` `claude` |
| **awesome-copilot** | [github/awesome-copilot](https://github.com/github/awesome-copilot) | Community instructions, agents, skills for GitHub Copilot | `curated-list` `copilot` |

---

## Design Patterns Across Agent CLIs

Common architectural patterns observed across all agent-native CLIs:

| Pattern | Description | Examples |
|---------|-------------|----------|
| **Structured JSON Output** | Every response is parseable JSON/NDJSON | All workspace CLIs |
| **`--dry-run`** | Preview destructive operations | gws, lark-cli, dws |
| **Three-Layer Architecture** | Shortcuts → API commands → Raw API | lark-cli, dws |
| **Bundled Skills** | SKILL.md files with `npx skills add` | gws, lark-cli, dws |
| **OAuth Device Flow** | Headless auth for agents | gws, lark-cli |
| **Auto-Pagination** | `--page-all` with NDJSON streaming | gws, lark-cli |
| **Discovery-Driven** | Commands built from API specs at runtime | gws, dws |
| **Output Formats** | `--format json\|table\|csv\|yaml\|ndjson` | Most CLIs |
| **Identity Switching** | `--as user` / `--as bot` | lark-cli |
| **Encrypted Credential Storage** | OS keyring or AES-256-GCM at rest | gws, dws |

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

Found a CLI that should be listed here? PRs welcome!

### Criteria for inclusion:
1. **CLI-first** — must be usable from the command line
2. **Agent-friendly** — structured output (JSON), or bundled agent skills, or designed for programmatic use
3. **Maintained** — actively maintained (commits in last 6 months)
4. **Open source** or has a free tier

### How to contribute:
1. Fork this repo
2. Add your CLI to the appropriate category table
3. Include: name, repo link, install command, language, tags
4. Submit a PR with a brief description of why it qualifies

---

## License

[MIT](LICENSE)

---

*Curated by [@shuyhere](https://github.com/shuyhere) — built with the help of AI agents, for AI agents.* 🔬
