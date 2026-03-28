<p align="center">
  <h1 align="center">Awesome Agent CLI</h1>
  <p align="center">
    <em>A curated collection of CLI tools and applications designed for AI agents.</em>
  </p>
  <p align="center">
    <a href="#productivity-suites">Productivity</a> &middot;
    <a href="#project-management">Project Mgmt</a> &middot;
    <a href="#knowledge--docs">Knowledge</a> &middot;
    <a href="#research--academic">Research</a> &middot;
    <a href="#email">Email</a> &middot;
    <a href="#social--messaging">Social</a> &middot;
    <a href="#developer-tools">Dev Tools</a> &middot;
    <a href="#browser--web-automation">Browser</a> &middot;
    <a href="#agent-applications">Agent Apps</a> &middot;
    <a href="#agent-bridges">Bridges</a>
  </p>
</p>

---

## What is an "Agent CLI"?

A new wave of command-line tools built specifically for **AI agents** (Claude Code, OpenClaw, Codex, Gemini CLI, Cursor, etc.) to interact with external services. Instead of raw REST APIs or bloated MCP servers, agent CLIs provide:

- **Structured JSON output** -- machine-parseable by default
- **Shell-composable commands** -- pipe, batch, combine
- **Safety features** -- `--dry-run`, input sanitization, scoped auth
- **Token-efficient** -- compact output for minimal context usage

This repo classifies and tags every known agent-friendly CLI so you can find the right tool for your agent stack.

---

## Tags Legend

| Tag | Meaning |
|-----|---------|
| `official` | Maintained by the platform vendor |
| `community` | Community-maintained |
| `agent-first` | Designed primarily for AI agents |
| `agent-friendly` | Works well with agents but not exclusively designed for them |
| `research` | Academic / research workflows |
| `productivity` | Workplace productivity (docs, calendar, email) |
| `project-mgmt` | Project and issue tracking |
| `knowledge` | Knowledge bases, wikis, notes |
| `messaging` | Chat and messaging platforms |
| `social` | Social media platforms |
| `dev-tools` | Developer-focused tools |
| `browser` | Web browsing and automation |
| `agent-app` | Full application designed for agent use |
| `bridge` | Connects agents to messaging platforms |
| `markdown` | Strong Markdown support / conversion |
| `batch-ops` | Supports batch operations for fewer tool calls |
| `token-efficient` | Specifically optimized for minimal token usage |

---

## Productivity Suites

| Name | Repo | Stars | Language | Tags | Description |
|------|------|-------|----------|------|-------------|
| **gws** | [googleworkspace/cli](https://github.com/googleworkspace/cli) | ![](https://img.shields.io/github/stars/googleworkspace/cli?style=flat-square) | Rust | `official` `agent-first` `productivity` `batch-ops` | One CLI for all of Google Workspace. Dynamic command surface from Discovery Service. Three-layer architecture: shortcuts (`+send`, `+agenda`) -> API methods -> raw API. Schema introspection, NDJSON streaming, encrypted OAuth. Install: `npm i -g @googleworkspace/cli` |
| **lark-cli** | [larksuite/cli](https://github.com/larksuite/cli) | ![](https://img.shields.io/github/stars/larksuite/cli?style=flat-square) | Go | `official` `agent-first` `productivity` `batch-ops` | Official Lark/Feishu CLI. 200+ commands, 11 domains (Calendar, Messenger, Docs, Drive, Base, Sheets, Tasks, Wiki, Contact, Mail, Meetings). Three-layer commands, non-blocking agent auth (`--no-wait`), schema introspection, `--dry-run`. Install: `npm i -g @larksuite/cli` |
| **feishu-cli** | [riba2534/feishu-cli](https://github.com/riba2534/feishu-cli) | ![](https://img.shields.io/github/stars/riba2534/feishu-cli?style=flat-square) | Go | `community` `agent-first` `productivity` `markdown` | Community Feishu CLI. Bidirectional lossless Markdown-to-Feishu conversion (40+ block types). Mermaid/PlantUML to editable Feishu Whiteboard. Concurrent pipeline tested at 10,000+ lines. Full platform coverage. Install: `curl -fsSL .../install.sh \| bash` |
| **Feishu-MCP** | [cso1z/Feishu-MCP](https://github.com/cso1z/Feishu-MCP) | ![](https://img.shields.io/github/stars/cso1z/Feishu-MCP?style=flat-square) | TypeScript | `community` `agent-friendly` `productivity` | Feishu/Lark MCP server + CLI. Integrates with Cursor, Claude Code, Cline. |

---

## Project Management

| Name | Repo | Stars | Language | Tags | Description |
|------|------|-------|----------|------|-------------|
| **linearis** | [czottmann/linearis](https://github.com/czottmann/linearis) | ![](https://img.shields.io/github/stars/czottmann/linearis?style=flat-square) | TypeScript | `community` `agent-first` `project-mgmt` `token-efficient` | Linear.app CLI. JSON output, smart ID resolution (`ABC-123` format). Under 1,000 tokens for agent context (vs ~13k for Linear MCP). Issues, Comments, Documents, Projects, Cycles, Embeds. Install: `npm i -g linearis` |
| **linctl** | [dorkitude/linctl](https://github.com/dorkitude/linctl) | ![](https://img.shields.io/github/stars/dorkitude/linctl?style=flat-square) | Go | `community` `agent-friendly` `project-mgmt` | Linear CLI built with agents in mind, Cobra framework. |
| **linear-cli** | [mixpeek/linear-cli](https://github.com/mixpeek/linear-cli) | ![](https://img.shields.io/github/stars/mixpeek/linear-cli?style=flat-square) | TypeScript | `community` `agent-friendly` `project-mgmt` | CLI tool for interacting with Linear.app. |

---

## Knowledge & Docs

| Name | Repo | Stars | Language | Tags | Description |
|------|------|-------|----------|------|-------------|
| **notion-cli-agent** | [Balneario-de-Cofrentes/notion-cli-agent](https://github.com/Balneario-de-Cofrentes/notion-cli-agent) | ![](https://img.shields.io/github/stars/Balneario-de-Cofrentes/notion-cli-agent?style=flat-square) | TypeScript | `community` `agent-first` `knowledge` `batch-ops` `token-efficient` | Notion CLI with `--llm` mode for compact output. Natural language queries (`notion find`), batch operations, workspace auto-discovery, Obsidian sync. Install: `npm i -g notion-cli-agent` |
| **vibe-notion** | [devxoul/vibe-notion](https://github.com/devxoul/vibe-notion) | ![](https://img.shields.io/github/stars/devxoul/vibe-notion?style=flat-square) | TypeScript | `community` `agent-first` `knowledge` | Notion automation CLI for AI agents. |
| **notion-cli** | [Coastal-Programs/notion-cli](https://github.com/Coastal-Programs/notion-cli) | ![](https://img.shields.io/github/stars/Coastal-Programs/notion-cli?style=flat-square) | Go | `community` `agent-first` `knowledge` | Enterprise-grade Notion CLI. Advanced retry, caching. |
| **feishu-docx** | [leemysw/feishu-docx](https://github.com/leemysw/feishu-docx) | ![](https://img.shields.io/github/stars/leemysw/feishu-docx?style=flat-square) | Python | `community` `agent-friendly` `knowledge` `markdown` | Feishu/Lark Docs and Sheets to Markdown with OAuth, CLI, TUI. |
| **obsidian-export** | [zoni/obsidian-export](https://github.com/zoni/obsidian-export) | ![](https://img.shields.io/github/stars/zoni/obsidian-export?style=flat-square) | Rust | `community` `agent-friendly` `knowledge` `markdown` | Export Obsidian vault to regular Markdown. Resolves wiki-links, embeds, and Obsidian-specific syntax. |
| **ov** | [sokojh/obsidian-vault](https://github.com/sokojh/obsidian-vault) | ![](https://img.shields.io/github/stars/sokojh/obsidian-vault?style=flat-square) | Rust | `community` `agent-first` `knowledge` | Agent-first CLI for Obsidian vaults. JSON-only output, schema introspection, `--dry-run` safety. |
| **obs** | [markfive-proto/obsidian-vault-cli](https://github.com/markfive-proto/obsidian-vault-cli) | ![](https://img.shields.io/github/stars/markfive-proto/obsidian-vault-cli?style=flat-square) | TypeScript | `community` `agent-friendly` `knowledge` | Community CLI for Obsidian vaults. 100+ commands for notes, search, tags, links, tasks. |
| **obsidianRAGsody** | [nicolaischneider/obsidianRAGsody](https://github.com/nicolaischneider/obsidianRAGsody) | ![](https://img.shields.io/github/stars/nicolaischneider/obsidianRAGsody?style=flat-square) | Python | `community` `agent-friendly` `knowledge` | CLI for intelligent Obsidian vault interaction using RAG. Natural language queries, URL-to-markdown conversion. |

---

## Research & Academic

| Name | Repo | Stars | Language | Tags | Description |
|------|------|-------|----------|------|-------------|
| **pyoverleaf** | [jkulhanek/pyoverleaf](https://github.com/jkulhanek/pyoverleaf) | ![](https://img.shields.io/github/stars/jkulhanek/pyoverleaf?style=flat-square) | Python | `community` `agent-friendly` `research` `markdown` | Python API and CLI for Overleaf. List/create/archive projects, upload/download files, comments, live changes. Auth via browser cookies. Install: `pip install pyoverleaf` |
| **olcli** | [aloth/olcli](https://github.com/aloth/olcli) | ![](https://img.shields.io/github/stars/aloth/olcli?style=flat-square) | JavaScript | `community` `agent-friendly` `research` | Overleaf CLI. Sync, manage, and compile LaTeX projects from terminal. |
| **overleaf-sync-rs** | [katzper-michno/overleaf-sync-rs](https://github.com/katzper-michno/overleaf-sync-rs) | ![](https://img.shields.io/github/stars/katzper-michno/overleaf-sync-rs?style=flat-square) | Rust | `community` `agent-friendly` `research` | Bidirectional sync between Overleaf and local filesystem. |
| **overleap** | [Axect/overleap](https://github.com/Axect/overleap) | ![](https://img.shields.io/github/stars/Axect/overleap?style=flat-square) | JavaScript | `community` `agent-friendly` `research` | Real-time bidirectional Overleaf sync. Leap over the browser. |
| **LeafLink** | [xiongqi123123/LeafLink](https://github.com/xiongqi123123/LeafLink) | ![](https://img.shields.io/github/stars/xiongqi123123/LeafLink?style=flat-square) | Python | `community` `agent-friendly` `research` | Lightweight Overleaf sync CLI. Pull/push workflows, pseudo real-time collaboration. |
| **overleaf-cli** | [BruceChenSF/overleaf-cli](https://github.com/BruceChenSF/overleaf-cli) | ![](https://img.shields.io/github/stars/BruceChenSF/overleaf-cli?style=flat-square) | TypeScript | `community` `agent-first` `research` | Enable AI tools (Claude Code, Cursor) to directly edit Overleaf projects via local file sync. |
| **pubtab** | [Galaxy-Dawn/pubtab](https://github.com/Galaxy-Dawn/pubtab) | ![](https://img.shields.io/github/stars/Galaxy-Dawn/pubtab?style=flat-square) | Python | `community` `agent-friendly` `research` | Bidirectional Excel-to-LaTeX table converter with style-preserving roundtrip and PNG/PDF preview. |
| **xiv** | [james-akl/xiv](https://github.com/james-akl/xiv) | ![](https://img.shields.io/github/stars/james-akl/xiv?style=flat-square) | Python | `community` `agent-friendly` `research` | Minimal arXiv search and download CLI. |
| **Research-Paper-Extractor** | [Sreeram5678/Research-Paper-Extractor](https://github.com/Sreeram5678/Research-Paper-Extractor) | ![](https://img.shields.io/github/stars/Sreeram5678/Research-Paper-Extractor?style=flat-square) | Python | `community` `agent-friendly` `research` | Automated arXiv paper search and download. Search by keywords, authors, categories. |
| **rSearch** | [jscraik/rSearch](https://github.com/jscraik/rSearch) | ![](https://img.shields.io/github/stars/jscraik/rSearch?style=flat-square) | TypeScript | `community` `agent-friendly` `research` | Search, fetch, and download arXiv papers from the terminal. |
| **searchkit** | [RanaPriyansh/searchkit](https://github.com/RanaPriyansh/searchkit) | ![](https://img.shields.io/github/stars/RanaPriyansh/searchkit?style=flat-square) | Python | `community` `agent-friendly` `research` | Academic paper discovery and summarization CLI. Search arXiv, PubMed, SSRN; download PDFs; generate summaries. |
| **s2cli** | [mrshu/s2cli](https://github.com/mrshu/s2cli) | ![](https://img.shields.io/github/stars/mrshu/s2cli?style=flat-square) | Python | `community` `agent-first` `research` | CLI for the Semantic Scholar API. Designed for both human researchers and AI agents. |
| **PaperHunterAgent** | [madara88645/PaperHunterAgent](https://github.com/madara88645/PaperHunterAgent) | ![](https://img.shields.io/github/stars/madara88645/PaperHunterAgent?style=flat-square) | Python | `community` `agent-first` `research` | Multi-agent CLI. Discovers, summarizes, and visualizes papers from arXiv and Semantic Scholar. |
| **arxiv-cli** | [lucabeetz/arxiv-cli](https://github.com/lucabeetz/arxiv-cli) | ![](https://img.shields.io/github/stars/lucabeetz/arxiv-cli?style=flat-square) | Rust | `community` `agent-friendly` `research` | Small CLI to search and download arXiv papers. |

---

## Email

| Name | Repo | Stars | Language | Tags | Description |
|------|------|-------|----------|------|-------------|
| **himalaya** | [pimalaya/himalaya](https://github.com/pimalaya/himalaya) | ![](https://img.shields.io/github/stars/pimalaya/himalaya?style=flat-square) | Rust | `community` `agent-friendly` `productivity` | CLI for IMAP/SMTP email. List, read, write, reply, forward, search, organize. Multi-account, MML composition. Install: `brew install himalaya` |
| **Gmail via gws** | [googleworkspace/cli](https://github.com/googleworkspace/cli) | ![](https://img.shields.io/github/stars/googleworkspace/cli?style=flat-square) | Rust | `official` `agent-first` `productivity` | Gmail through Google Workspace CLI: `gws gmail +send`, `+reply`, `+triage`, `+watch`. See Productivity Suites. |

---

## Social & Messaging

| Name | Repo | Stars | Language | Tags | Description |
|------|------|-------|----------|------|-------------|
| **xurl** | (OpenClaw built-in) | -- | -- | `community` `agent-friendly` `social` | X/Twitter API v2 CLI. Post tweets, reply, quote, search, DMs, media upload. |
| **wacli** | (OpenClaw built-in) | -- | -- | `community` `agent-friendly` `messaging` | WhatsApp CLI. Send messages, search/sync history. |
| **slack-rs** | [tumf/slack-rs](https://github.com/tumf/slack-rs) | ![](https://img.shields.io/github/stars/tumf/slack-rs?style=flat-square) | Rust | `community` `agent-first` `messaging` | Slack CLI with OAuth auth, agentic design principles. |

---

## Developer Tools

| Name | Repo | Stars | Language | Tags | Description |
|------|------|-------|----------|------|-------------|
| **gh** | [cli/cli](https://github.com/cli/cli) | ![](https://img.shields.io/github/stars/cli/cli?style=flat-square) | Go | `official` `agent-friendly` `dev-tools` | GitHub CLI. Issues, PRs, CI/CD, code review, releases, API queries, gists, repos. Install: `brew install gh` |

---

## Browser & Web Automation

| Name | Repo | Stars | Language | Tags | Description |
|------|------|-------|----------|------|-------------|
| **browser-use** | [browser-use/browser-use](https://github.com/browser-use/browser-use) | ![](https://img.shields.io/github/stars/browser-use/browser-use?style=flat-square) | Python | `community` `agent-first` `browser` | Make websites accessible for AI agents. Automate tasks online. The most popular agent browser library. |
| **UI-TARS-desktop** | [bytedance/UI-TARS-desktop](https://github.com/bytedance/UI-TARS-desktop) | ![](https://img.shields.io/github/stars/bytedance/UI-TARS-desktop?style=flat-square) | TypeScript | `official` `agent-first` `browser` `agent-app` | Open-source multimodal AI agent stack from ByteDance. Connecting AI models and agent infrastructure. |
| **nanobrowser** | [nanobrowser/nanobrowser](https://github.com/nanobrowser/nanobrowser) | ![](https://img.shields.io/github/stars/nanobrowser/nanobrowser?style=flat-square) | TypeScript | `community` `agent-first` `browser` | Chrome extension for AI-powered web automation. Multi-agent workflows with your own LLM API key. |
| **magentic-ui** | [microsoft/magentic-ui](https://github.com/microsoft/magentic-ui) | ![](https://img.shields.io/github/stars/microsoft/magentic-ui?style=flat-square) | Python | `official` `agent-first` `browser` | Human-centered web agent research prototype from Microsoft. |
| **wiseflow** | [TeamWiseFlow/wiseflow](https://github.com/TeamWiseFlow/wiseflow) | ![](https://img.shields.io/github/stars/TeamWiseFlow/wiseflow?style=flat-square) | JavaScript | `community` `agent-friendly` `browser` | Enhance any agent's browser use skill. |
| **openbrowser** | [ntegrals/openbrowser](https://github.com/ntegrals/openbrowser) | ![](https://img.shields.io/github/stars/ntegrals/openbrowser?style=flat-square) | TypeScript | `community` `agent-first` `browser` | Autonomous toolkit for browser-based AI agents. |
| **notte** | [nottelabs/notte](https://github.com/nottelabs/notte) | ![](https://img.shields.io/github/stars/nottelabs/notte?style=flat-square) | Python | `community` `agent-first` `browser` | Framework to build web agents and deploy serverless web automation on reliable browser infra. |
| **agentql** | [tinyfish-io/agentql](https://github.com/tinyfish-io/agentql) | ![](https://img.shields.io/github/stars/tinyfish-io/agentql?style=flat-square) | Python | `community` `agent-first` `browser` | Suite of tools for connecting AI to the web. Query language and Playwright integrations. |
| **HyperAgent** | [hyperbrowserai/HyperAgent](https://github.com/hyperbrowserai/HyperAgent) | ![](https://img.shields.io/github/stars/hyperbrowserai/HyperAgent?style=flat-square) | TypeScript | `community` `agent-first` `browser` | AI browser automation. |
| **browserable** | [browserable/browserable](https://github.com/browserable/browserable) | ![](https://img.shields.io/github/stars/browserable/browserable?style=flat-square) | JavaScript | `community` `agent-first` `browser` | Open source and self-hostable browser automation library for AI agents. |
| **AIPex** | [AIPexStudio/AIPex](https://github.com/AIPexStudio/AIPex) | ![](https://img.shields.io/github/stars/AIPexStudio/AIPex?style=flat-square) | TypeScript | `community` `agent-first` `browser` | AI browser automation assistant. Privacy first, no migration. |
| **fara** | [microsoft/fara](https://github.com/microsoft/fara) | ![](https://img.shields.io/github/stars/microsoft/fara?style=flat-square) | Python | `official` `agent-first` `browser` | Fara-7B: efficient agentic model for computer use, from Microsoft. |
| **mobile-use** | [minitap-ai/mobile-use](https://github.com/minitap-ai/mobile-use) | ![](https://img.shields.io/github/stars/minitap-ai/mobile-use?style=flat-square) | Python | `community` `agent-first` `browser` `agent-app` | AI agents use real Android and iOS apps, just like a human. |
| **agent-browser-go** | [cpunion/agent-browser-go](https://github.com/cpunion/agent-browser-go) | ![](https://img.shields.io/github/stars/cpunion/agent-browser-go?style=flat-square) | Go | `community` `agent-first` `browser` | Headless browser automation CLI for AI agents. chromedp/playwright backends. |

---

## Agent Applications

Applications and plugins specifically designed for agent integration.

| Name | Repo | Stars | Language | Tags | Description |
|------|------|-------|----------|------|-------------|
| **obsidian-skills** | [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills) | ![](https://img.shields.io/github/stars/kepano/obsidian-skills?style=flat-square) | -- | `official` `agent-first` `agent-app` `knowledge` | Official agent skills for Obsidian. Teach your agent to use Markdown, Bases, JSON Canvas, and the CLI. |
| **obsidian-agent-client** | [RAIT-09/obsidian-agent-client](https://github.com/RAIT-09/obsidian-agent-client) | ![](https://img.shields.io/github/stars/RAIT-09/obsidian-agent-client?style=flat-square) | TypeScript | `community` `agent-first` `agent-app` `knowledge` | Bring AI agents into Obsidian via Agent Client Protocol (ACP). Supports Claude Code, Codex, Gemini CLI. |
| **geminese** | [Momoyu404/geminese](https://github.com/Momoyu404/geminese) | ![](https://img.shields.io/github/stars/Momoyu404/geminese?style=flat-square) | TypeScript | `community` `agent-first` `agent-app` `knowledge` | Obsidian plugin that embeds Gemini CLI as AI collaborator in your vault. |
| **neurostack** | [raphasouthall/neurostack](https://github.com/raphasouthall/neurostack) | ![](https://img.shields.io/github/stars/raphasouthall/neurostack?style=flat-square) | Python | `community` `agent-first` `agent-app` `knowledge` | CLI + MCP server to build, maintain, and search a knowledge vault. Second brain starting today. |
| **plandex** | [plandex-ai/plandex](https://github.com/plandex-ai/plandex) | ![](https://img.shields.io/github/stars/plandex-ai/plandex?style=flat-square) | Go | `community` `agent-first` `agent-app` `dev-tools` | Open source AI coding agent. Designed for large projects and real world tasks. |
| **superset** | [superset-sh/superset](https://github.com/superset-sh/superset) | ![](https://img.shields.io/github/stars/superset-sh/superset?style=flat-square) | TypeScript | `community` `agent-first` `agent-app` `dev-tools` | Code editor for the AI agents era. Run an army of Claude Code, Codex, etc. on your machine. |
| **axe** | [jrswab/axe](https://github.com/jrswab/axe) | ![](https://img.shields.io/github/stars/jrswab/axe?style=flat-square) | Go | `community` `agent-first` `agent-app` | Lightweight CLI for running single-purpose AI agents. Define focused agents in TOML, trigger from anywhere (pipes, git hooks, cron). |
| **dataclaw-sync** | [UFOyyds/dataclaw-sync](https://github.com/UFOyyds/dataclaw-sync) | ![](https://img.shields.io/github/stars/UFOyyds/dataclaw-sync?style=flat-square) | Python | `community` `agent-friendly` `agent-app` `knowledge` | Incremental export of AI agent conversations to Obsidian notes. Supports Claude Code, OpenCode, Codex, Gemini CLI, OpenClaw. |

---

## Agent Bridges

Tools that connect coding agents to messaging platforms.

| Name | Repo | Stars | Language | Tags | Description |
|------|------|-------|----------|------|-------------|
| **cc-connect** | [chenhg5/cc-connect](https://github.com/chenhg5/cc-connect) | ![](https://img.shields.io/github/stars/chenhg5/cc-connect?style=flat-square) | Go | `community` `bridge` `messaging` | Bridge coding agents (Claude Code, Cursor, Gemini CLI, Codex) to Feishu/Lark, DingTalk, Slack, Telegram, Discord. |
| **golembot** | [0xranx/golembot](https://github.com/0xranx/golembot) | ![](https://img.shields.io/github/stars/0xranx/golembot?style=flat-square) | TypeScript | `community` `bridge` `messaging` | Any Agent, Any Provider, Anywhere. Cursor, Claude Code, OpenCode, Codex to Slack, Telegram, Discord, Feishu, DingTalk, WeCom. |
| **feishu-claude-code** | [joewongjc/feishu-claude-code](https://github.com/joewongjc/feishu-claude-code) | ![](https://img.shields.io/github/stars/joewongjc/feishu-claude-code?style=flat-square) | Python | `community` `bridge` `messaging` | Bridge Claude Code CLI with Feishu/Lark via WebSocket. |

---

## Design Patterns

The best agent CLIs share these design principles:

**Output** -- JSON by default + `--format table|csv|ndjson`. `--llm` mode for token-efficient output. NDJSON streaming for paginated results.

**Command Architecture** -- Three-layer pattern (lark-cli, gws): Shortcuts (`+agenda`, `+send`) -> API commands (1:1 with endpoints) -> Raw API (full coverage). Schema introspection for agents to discover parameters.

**Auth** -- Non-blocking auth that returns URL for human to approve. Environment variables as primary method. OS keyring for credential storage.

**Agent Integration** -- Batch operations to minimize tool calls. `--dry-run` for safety. Progressive disclosure with small context docs + on-demand references.

---

## Gaps & Opportunities

Services that don't yet have a good agent-friendly CLI:

| Service | Status |
|---------|--------|
| Jira | Community CLIs exist, none agent-optimized |
| Confluence | No agent CLI |
| Asana | No known agent CLI |
| Trello | No agent CLI |
| Todoist | Has CLI, not agent-designed |
| Airtable | No agent CLI |
| Figma | No CLI (API exists) |
| Zoom | No agent CLI |
| HuggingFace | huggingface-cli exists, not agent-optimized |

---

## Contributing

Know an agent-friendly CLI that is missing? Open a PR.

**Inclusion criteria:**
1. Must be a CLI tool or application designed for agent use
2. Must work well with AI agents (structured output, composable commands)
3. Must have its own repository link

**Format:** Add a row to the appropriate category table: Name, Repo link, shields.io star badge, Language, Tags, Description.

Star badge format: `![](https://img.shields.io/github/stars/OWNER/REPO?style=flat-square)`

---

## License

This collection is [CC0 1.0 Universal](LICENSE) -- public domain. Individual tools have their own licenses.

---

<p align="center">
  Curated by <a href="https://github.com/shuyhere">@shuyhere</a>
</p>
