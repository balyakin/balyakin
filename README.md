# Evgeny Balyakin

Developer. I build small tools, usually because I got annoyed by something.

Most of what's here is Go, Rust, or TypeScript. A lot of CLIs. SQLite wherever I can avoid running a server.

[![GitHub followers](https://img.shields.io/github/followers/balyakin?label=Follow&style=social)](https://github.com/balyakin)

---

## Things I've built

**[aishield](https://github.com/balyakin/aishield)** — Safety layer for AI coding agents: blocks dangerous shell commands, strips secrets before they reach the agent context, keeps a JSONL audit log. Started this after an agent deleted a directory I hadn't committed yet. Go.

**[llmfail](https://github.com/balyakin/llmfail)** — Local proxy that adds failover between LLM providers. Anthropic returning 429s? Falls through to OpenAI or wherever. Mostly just a routing layer, smaller than you'd expect. Go.

**[codebone](https://github.com/balyakin/codebone)** — CLI and MCP server for giving agents compact code context. Extracts symbols, signatures, and structure with tree-sitter instead of dumping whole files. TypeScript.

**[sqliteq](https://github.com/balyakin/sqliteq)** — Job queues, pub/sub, and scheduled jobs inside a single SQLite file. No daemon, no Redis. Just a file. Rust.

**[snapback](https://github.com/balyakin/snapback)** — Incremental local backups for project folders. Per-file deduplication, SQLite index, and restore by date or file when you need to rewind without thinking about it. Python.

**[tokmon](https://github.com/balyakin/tokmon)** — Proxy for tracking token usage and costs across Anthropic/OpenAI. If you run a lot of agents you'll want this before the invoice arrives. Go, SQLite.

**[sudocheck](https://github.com/balyakin/sudocheck)** — Linux privilege escalation audit: sudo rules, SUID/SGID binaries, capabilities, GTFOBins cross-reference. Outputs JSON or SARIF. Go.

**[depshield](https://github.com/balyakin/depshield)** — Supply-chain check for package managers. One command, works across npm/pip/cargo/etc. Go.

**[git-pulse](https://github.com/balyakin/git-pulse)** — Codebase diagnostics from git history: churn, ownership, dead zones. Rust, TUI.

**[TubeSift](https://github.com/balyakin/TubeSift)** — Search YouTube channels by subtitle content, from the terminal. Full-text index. Python, SQLite.

---

## Stack

Go for most backend tooling. Rust when I want small binaries or need the performance. Python for scripting and quick prototypes. SQLite as default storage — you can get surprisingly far without running a server.

---

## Elsewhere

I also built [SkyMoment](https://skymoment.art) — generates personalized star map posters. Very different from everything else here, but it's mine.
