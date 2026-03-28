# Awesome Agent CLI

> A curated collection of CLI tools and applications designed for AI agents — classified by domain, with tags, install commands, and auto-updating star counts.

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
- [Note-taking and Knowledge Management](#note-taking-and-knowledge-management)
- [Browser Automation for Agents](#browser-automation-for-agents)
- [Smart Home and IoT](#smart-home-and-iot)
- [Coding Agents](#coding-agents)
- [Agent Infrastructure](#agent-infrastructure)
- [Design Patterns](#design-patterns-across-agent-clis)
- [Tags Reference](#tags-reference)
- [Contributing](#contributing)

---

## Workspace and Productivity Suites

Full SaaS platform CLIs with broad API coverage.

| CLI | Stars | Install | Lang | Description | Tags |
|-----|-------|---------|------|-------------|------|
| [gws](https://github.com/googleworkspace/cli) | ![Stars](https://img.shields.io/github/stars/googleworkspace/cli?style=flat&label=) | `npm i -g @googleworkspace/cli` | Rust | Google Workspace CLI. Dynamically generates commands from Google's Discovery Service — new APIs are picked up automatically. Covers Gmail, Drive, Calendar, Sheets, Docs, Chat, Admin, and 85+ APIs. Ships 100+ agent skills, helper commands (`gws gmail +send`, `gws calendar +agenda`), three auth flows (interactive OAuth, service account, pre-obtained token). | `productivity` `email` `calendar` `docs` `sheets` `drive` `chat` |
| [lark-cli](https://github.com/larksuite/cli) | ![Stars](https://img.shields.io/github/stars/larksuite/cli?style=flat&label=) | `npm i -g @larksuite/cli` | Go | Official Feishu/Lark CLI from ByteDance. Three-layer architecture: shortcut commands (human+AI friendly), API commands (platform-synced), raw API (2500+ endpoints). 200+ commands covering Messenger, Docs, Base, Sheets, Calendar, Mail, Tasks, Meetings. Supports `--dry-run`, identity switching (`--as user` / `--as bot`), 19 agent skills. | `productivity` `messenger` `docs` `sheets` `calendar` `mail` `tasks` `meetings` `china` |
| [dws](https://github.com/DingTalk-Real-AI/dingtalk-workspace-cli) | ![Stars](https://img.shields.io/github/stars/DingTalk-Real-AI/dingtalk-workspace-cli?style=flat&label=) | `curl -fsSL .../install.sh \| sh` | Go | Official DingTalk CLI. Uses discovery-driven MCP (Model Context Protocol) JSON-RPC pipeline — commands built from market registry, not hardcoded. Covers Contacts, Calendar, Todo, Attendance, Chat, Approval, Base. Currently in co-creation phase (whitelist required). | `productivity` `contacts` `calendar` `todo` `attendance` `chat` `china` `mcp` |

---

## Meta-CLIs and Universal Hubs

Tools that wrap multiple services or turn arbitrary interfaces into CLIs.

| CLI | Stars | Install | Lang | Description | Tags |
|-----|-------|---------|------|-------------|------|
| [OpenCLI](https://github.com/jackwener/opencli) | ![Stars](https://img.shields.io/github/stars/jackwener/opencli?style=flat&label=) | `npm i -g @jackwener/opencli` | TypeScript | Turns any website, Electron app, or local CLI into a unified CLI. 65+ site adapters (Bilibili, Twitter/X, Reddit, Xiaohongshu, YouTube). Wraps Electron apps (Cursor, ChatGPT, Notion, Discord) via CDP. Zero LLM cost — deterministic output. Passthrough hub for `gh`, `gws`, `docker` with auto-install. Anti-detection built in. | `meta-cli` `browser` `scraping` `social-media` `electron` `hub` |
| [x-cmd](https://github.com/x-cmd/x-cmd) | ![Stars](https://img.shields.io/github/stars/x-cmd/x-cmd?style=flat&label=) | `eval "$(curl https://get.x-cmd.com)"` | Awk | Bootstrap 1000+ CLI tools in seconds. Package manager + 100+ functional modules. Provides `llms.txt` manifest for agent discovery. No-sudo, pure awk core engine under 1MB. Great for provisioning agent environments. | `meta-cli` `package-manager` `1000+-tools` `agent-bootstrap` |

---

## Research and Academic

Tools for academic workflows: paper search, LaTeX, literature management, publishing.

| CLI | Stars | Install | Lang | Description | Tags |
|-----|-------|---------|------|-------------|------|
| [olcli](https://github.com/aloth/olcli) | ![Stars](https://img.shields.io/github/stars/aloth/olcli?style=flat&label=) | `npm i -g @aloth/olcli` | TypeScript | Overleaf CLI. Sync LaTeX projects from the command line — pull projects locally, push changes back, compile PDFs, download `.bbl` files for arXiv submissions. Essential for agent-driven paper writing without the Overleaf web UI. | `research` `latex` `overleaf` `papers` `arxiv` `collaboration` |
| [papercli](https://github.com/jimezsa/papercli) | ![Stars](https://img.shields.io/github/stars/jimezsa/papercli?style=flat&label=) | `brew install jimezsa/tap/papercli` | Go | Search academic papers across arXiv, Semantic Scholar, and Google Scholar (via SerpApi). Three search modes: fast-search (3-6 papers), pro-search (8-12 papers with cross-paper comparison), deep-search (institutional-grade investigation). Download PDFs, search by author, track seen papers, export to Markdown/CSV/JSON. | `research` `papers` `arxiv` `semantic-scholar` `google-scholar` `search` `literature` |

---

## Developer Tools

Code hosting, CI/CD, version control, and dev infrastructure.

| CLI | Stars | Install | Lang | Description | Tags |
|-----|-------|---------|------|-------------|------|
| [gh](https://github.com/cli/cli) | ![Stars](https://img.shields.io/github/stars/cli/cli?style=flat&label=) | `brew install gh` | Go | The de facto standard GitHub CLI. Issues, PRs, CI runs, code review, API queries (`gh api`). Massive ecosystem of extensions. Every AI coding agent supports it natively. Structured JSON output via `--json`. | `developer` `github` `issues` `prs` `ci` `code-review` `api` |
| [xurl](https://github.com/user/xurl) | — | — | — | CLI tool for authenticated requests to the X (Twitter) API v2. Post tweets, reply, quote, search, read posts, manage followers, send DMs, upload media. | `developer` `social-media` `twitter` `api` |

---

## Social and Networking

CLIs for social platforms and professional networking.

| CLI | Stars | Install | Lang | Description | Tags |
|-----|-------|---------|------|-------------|------|
| [linkedin-cli](https://github.com/Linked-API/linkedin-cli) | ![Stars](https://img.shields.io/github/stars/Linked-API/linkedin-cli?style=flat&label=) | `npm i -g @linkedapi/linkedin-cli` | TypeScript | Cloud-browser-based LinkedIn automation via Linked API. Fetch profiles, search people/companies, send messages, manage connections, create posts, react, comment. Anti-detection built in (residential IPs, human-like patterns). Multi-account support. Structured JSON output. | `social` `networking` `linkedin` `profiles` `messaging` `job-search` |
| [OpenCLI social adapters](https://github.com/jackwener/opencli) | ![Stars](https://img.shields.io/github/stars/jackwener/opencli?style=flat&label=) | See OpenCLI above | TypeScript | 65+ site adapters for social platforms. Twitter trending/search/timeline/bookmarks/post, Reddit hot/frontpage/subreddit, Bilibili hot/search/history, Xiaohongshu search/feed/publish, YouTube, and more. Uses Chrome login session. | `social` `twitter` `reddit` `bilibili` `xiaohongshu` `youtube` |

---

## Communication and Email

Messaging, email, and chat CLIs.

| CLI | Stars | Install | Lang | Description | Tags |
|-----|-------|---------|------|-------------|------|
| [himalaya](https://github.com/pimalaya/himalaya) | ![Stars](https://img.shields.io/github/stars/pimalaya/himalaya?style=flat&label=) | `brew install himalaya` | Rust | Multi-account IMAP/SMTP email client for the terminal. Compose with MML (MIME Meta Language). List, read, write, reply, forward, search, and organize emails. Privacy-first, local-only. | `email` `imap` `smtp` `multi-account` `mml` |
| [gws gmail](https://github.com/googleworkspace/cli) | ![Stars](https://img.shields.io/github/stars/googleworkspace/cli?style=flat&label=) | See gws above | Rust | Gmail via Google Workspace CLI. Helper commands: `+send`, `+reply`, `+reply-all`, `+forward`, `+triage` (unread inbox summary), `+watch` (stream new emails as NDJSON). | `email` `gmail` `google` |
| [lark-cli im](https://github.com/larksuite/cli) | ![Stars](https://img.shields.io/github/stars/larksuite/cli?style=flat&label=) | See lark-cli above | Go | Feishu/Lark instant messaging. Send/reply messages, group chat management, message search, upload/download images and files, reactions. | `messaging` `feishu` `lark` `china` |

---

## Note-taking and Knowledge Management

CLIs for note-taking apps, knowledge bases, and persistent agent memory.

| CLI | Stars | Install | Lang | Description | Tags |
|-----|-------|---------|------|-------------|------|
| [notion-cli](https://github.com/4ier/notion-cli) | ![Stars](https://img.shields.io/github/stars/4ier/notion-cli?style=flat&label=) | `brew install 4ier/tap/notion-cli` | Go | Like `gh` for GitHub, but for Notion. 39 commands covering 100% of the Notion API. Manage pages, databases, blocks, comments, users, and files. Supports `--filter`, `--sort`, Markdown I/O (`--md`), auto-detected property types, raw API escape hatch. Single binary. | `notes` `notion` `databases` `pages` `blocks` `markdown` |
| [beacon](https://github.com/HenriqueSchroeder/beacon) | ![Stars](https://img.shields.io/github/stars/HenriqueSchroeder/beacon?style=flat&label=) | Build from source | Go | Fast, headless CLI for Obsidian vaults on servers. Read, search, and manage vault files without GUI. Designed for AI agent access to Obsidian knowledge bases on headless machines. | `notes` `obsidian` `headless` `vault` `knowledge-base` |
| [obsidian-vault-cli](https://github.com/fanselau/obsidian-vault-cli) | ![Stars](https://img.shields.io/github/stars/fanselau/obsidian-vault-cli?style=flat&label=) | `npm i -g obsidian-vault-cli` | TypeScript | Headless CLI for reading and writing encrypted Obsidian LiveSync vaults. Built specifically for AI agents. Supports encrypted vaults and LiveSync protocol. | `notes` `obsidian` `headless` `encrypted` `livesync` `agent-native` |
| [OpenContext](https://github.com/0xranx/OpenContext) | ![Stars](https://img.shields.io/github/stars/0xranx/OpenContext?style=flat&label=) | `npm i -g @aicontextlab/cli` | TypeScript | Personal context store for AI agents. Persistent memory across repos/sessions. CLI + MCP server + Desktop GUI + Web UI. "Load history first, then act; ship, then persist." Slash commands for Cursor, Claude Code, and Codex. Bring your own coding agent. | `knowledge` `memory` `context` `persistence` `cross-repo` `mcp` |

---

## Browser Automation for Agents

Browsers and automation frameworks purpose-built for AI agent control.

| Tool | Stars | Install | Lang | Description | Tags |
|------|-------|---------|------|-------------|------|
| [agent-browser](https://github.com/vercel-labs/agent-browser) | ![Stars](https://img.shields.io/github/stars/vercel-labs/agent-browser?style=flat&label=) | `npm i -g agent-browser` | Rust | Headless browser automation CLI from Vercel. Native Rust binary. Commands: `open`, `click`, `fill`, `snapshot` (accessibility tree with refs for AI), `screenshot`, `eval`, `find` (by ARIA role/text/label). Ref-based interaction: `agent-browser click @e2`. Downloads Chrome from Chrome for Testing. No Playwright or Node.js runtime needed. | `browser` `automation` `headless` `vercel` `accessibility` `agent-native` |
| [browser-use](https://github.com/browser-use/browser-use) | ![Stars](https://img.shields.io/github/stars/browser-use/browser-use?style=flat&label=) | `uv add browser-use` | Python | Make websites accessible for AI agents. LLM-driven browser automation with natural language tasks. Open source library + cloud option with stealth/proxy/captcha. 1000+ integrations. Persistent filesystem and memory. Benchmarked on 100 real-world tasks. | `browser` `automation` `llm-driven` `cloud` `stealth` |
| [stagehand](https://github.com/browserbase/stagehand) | ![Stars](https://img.shields.io/github/stars/browserbase/stagehand?style=flat&label=) | `npx create-browser-app` | TypeScript | AI browser automation framework. Combine natural language (`act()`, `agent()`) with code-level precision. `extract()` returns structured data via Zod schemas. Auto-caching + self-healing: runs without LLM inference on repeat, re-engages AI when pages change. Playwright-based. | `browser` `automation` `framework` `natural-language` `self-healing` `playwright` |

---

## Smart Home and IoT

Control physical devices from the command line.

| CLI | Stars | Install | Lang | Description | Tags |
|-----|-------|---------|------|-------------|------|
| [openhue](https://github.com/openhue/openhue-cli) | ![Stars](https://img.shields.io/github/stars/openhue/openhue-cli?style=flat&label=) | `brew install openhue` | Go | Control Philips Hue lights and scenes via CLI. Discover bridges, manage lights/rooms/zones, activate scenes, set brightness/color/temperature. | `smart-home` `lights` `hue` `scenes` `iot` |

---

## Coding Agents

Terminal-based AI coding assistants that act as CLI tools themselves.

| CLI | Stars | Install | Lang | Description | Tags |
|-----|-------|---------|------|-------------|------|
| [oh-my-pi](https://github.com/can1357/oh-my-pi) | ![Stars](https://img.shields.io/github/stars/can1357/oh-my-pi?style=flat&label=) | `npm i -g @oh-my-pi/pi-coding-agent` | TypeScript | Feature-rich coding agent. Hash-anchored edits, LSP integration (40+ languages), persistent Python IPython kernel, browser tools, subagents, TTSR (zero-context-use rules that inject only when needed), agentic git commits with hunk-level staging, custom skills/hooks. | `coding-agent` `lsp` `python` `browser` `subagents` `skills` |
| [Claude Code](https://github.com/anthropics/claude-code) | ![Stars](https://img.shields.io/github/stars/anthropics/claude-code?style=flat&label=) | `npm i -g @anthropic-ai/claude-code` | TypeScript | Anthropic's official coding agent for the terminal. File editing, shell commands, search, and multi-turn agentic loops. Supports skills, custom slash commands, hooks, and MCP tools. | `coding-agent` `anthropic` `terminal` `ai` |
| [Codex](https://github.com/openai/codex) | ![Stars](https://img.shields.io/github/stars/openai/codex?style=flat&label=) | `npm i -g @openai/codex` | TypeScript | OpenAI's coding agent CLI. Sandboxed execution, multi-model support, approval workflows for dangerous operations. | `coding-agent` `openai` `terminal` `ai` |
| [Gemini CLI](https://github.com/google/gemini-cli) | ![Stars](https://img.shields.io/github/stars/google/gemini-cli?style=flat&label=) | `npm i -g @google/gemini-cli` | TypeScript | Google's coding agent CLI. Gemini model access from the terminal with file context, shell integration, and extension support. | `coding-agent` `google` `terminal` `ai` |

---

## Agent Infrastructure

Runtimes, orchestrators, and platforms that host or coordinate agents.

| Tool | Stars | Install | Lang | Description | Tags |
|------|-------|---------|------|-------------|------|
| [OpenClaw](https://github.com/openclaw/openclaw) | ![Stars](https://img.shields.io/github/stars/openclaw/openclaw?style=flat&label=) | `npm i -g openclaw` | TypeScript | Agent runtime and orchestrator. Multi-channel (Discord, Telegram, WhatsApp, Signal, Slack, iMessage). Skills system, sub-agent spawning, ACP harness for coding agents, browser control, memory, heartbeats. | `agent-runtime` `orchestrator` `skills` `multi-channel` `discord` `telegram` `whatsapp` |
| [Forge](https://github.com/initializ/forge) | ![Stars](https://img.shields.io/github/stars/initializ/forge?style=flat&label=) | — | Go | OpenClaw for Enterprise. Secure, portable AI Agent runtime. Run agents locally, in cloud, or enterprise environments without inbound tunnels. Containerized deployment. | `agent-runtime` `enterprise` `containerized` `secure` |
| [refly](https://github.com/refly-ai/refly) | ![Stars](https://img.shields.io/github/stars/refly-ai/refly?style=flat&label=) | — | TypeScript | Open-source agent skills builder. Define skills by vibe workflow, run on Claude Code, Cursor, Codex, and more. Build bots for Slack, Lark/Feishu, and other platforms. | `skills-builder` `workflow` `multi-agent` |

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
| Ref-Based Interaction | Accessibility tree refs for AI (`@e2`) | agent-browser |
| Self-Healing | Cache actions, re-engage AI when page changes | stagehand |

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
| `notes` | Note-taking applications |
| `knowledge` | Knowledge management / memory |
| `browser` | Browser automation |
| `smart-home` | IoT / home automation |
| `coding-agent` | AI coding assistant |
| `agent-runtime` | Agent hosting / orchestration |
| `agent-native` | Purpose-built for AI agents |
| `meta-cli` | Wraps multiple tools/services |
| `china` | Primarily serves Chinese market |
| `mcp` | Uses Model Context Protocol |
| `hub` | Aggregates other CLIs |
| `skills-builder` | Creates/manages agent skills |
| `headless` | Runs without GUI / on servers |

---

## Contributing

Found a CLI that should be listed here? PRs welcome.

### Criteria for inclusion

1. **CLI-first** — must be usable from the command line (or expose a CLI interface)
2. **Agent-friendly** — structured output (JSON), or bundled agent skills, or designed for programmatic use
3. **Maintained** — actively maintained (commits in last 6 months)
4. **Open source** or has a free tier

### How to contribute

1. Fork this repo
2. Add your CLI to the appropriate category table
3. Include: name with repo link, install command, language, description, tags
4. Submit a PR with a brief description of why it qualifies

---

## License

[MIT](LICENSE)

---

*Curated by [@shuyhere](https://github.com/shuyhere) — built with the help of AI agents, for AI agents.*
