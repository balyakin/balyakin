# Evgeny Balyakin

Developer. I build small tools, usually because I got annoyed by something.

Most of what's here is Go, Rust, or TypeScript. A lot of CLIs. SQLite wherever I can avoid running a server.

[![GitHub followers](https://img.shields.io/github/followers/balyakin?label=Follow&style=social)](https://github.com/balyakin)

---

## Things I've built

**[aishield](https://github.com/balyakin/aishield)** — Safety layer for AI coding agents: blocks dangerous shell commands, strips secrets before they reach the agent context, keeps a JSONL audit log. Started this after an agent deleted a directory I hadn't committed yet. Go.

**[AgentFence](https://github.com/balyakin/agentfence)** — Seatbelt for the moment when "just point Codex at the repo" feels too trusting. Runs the agent in a shadow workspace, keeps `.env`, Git history, and `$HOME` out of reach, scans the result, and waits for you to apply the patch. Go.

**[SSH App Hub](https://github.com/balyakin/ssh-apphub)** — Local control panel for web apps already running on SSH hosts. Finds JupyterLab, TensorBoard, MLflow, Streamlit, Grafana, and code-server on a remote box, then opens them through ordinary OpenSSH tunnels so I can stop memorizing ports. Python.

**[incident-ci](https://github.com/balyakin/incident-ci)** — CI check for incident PRs, because "please fill out the incident notes" should not live in someone's memory. Keeps the Incident Card as Markdown in the repo, validates the YAML, and points GitHub annotations at the file reviewers are already approving. Python.

**[PgRelay](https://github.com/balyakin/pgrelay)** — Transactional outbox and background jobs for Python services already sitting on PostgreSQL. Enqueue work in the same SQLAlchemy transaction as the thing that caused it, then let a small asyncio worker handle retries, leases, dead-letter jobs, and replay. For when a webhook in the request is too flimsy, but adding a separate queue feels like punishment. Python.

**[refraction](https://github.com/balyakin/refraction)** — Offline scanner for hostile repository and package text that can derail AI-assisted review: prompt injection, refusal bait, obfuscated payloads, Trojan Source, and manifest tricks. Go.

**[dataminim](https://github.com/balyakin/dataminim)** — Offline scanner for the awkward database question: what PII and secrets are already in there? Reads PostgreSQL or SQLite metadata, samples bounded values, follows JSON paths, and writes console/JSON/HTML reports without exposing raw data. Go.

**[pr-audit](https://github.com/balyakin/pr-audit)** — Local-first CLI for reviewing large diffs. Finds risky changes hiding in noisy PRs: weakened tests, unsafe code, type suppressions, and secret-like values. TypeScript.

**[archlint](https://github.com/balyakin/archlint)** — Architecture drift starts as one harmless import. Define the layers in `archlint.yaml`; it checks Python, TypeScript, and JavaScript imports for boundary leaks, layer cycles, banned packages, and files that depend on too much. Deterministic CLI, no LLM. TypeScript.

**[tessera](https://github.com/balyakin/tessera)** — Publishing CLI for manuscripts that still live in Word or LibreOffice. Keeps named styles as meaning, so poems, letters, epigraphs, and bits of foreign text don't get flattened into "some italics with indentation". Builds EPUB, LaTeX, and PDF from the same DOCX/ODT source. Go.

**[mergetyp](https://github.com/balyakin/mergetyp)** — Mail-merge for PDFs when the template deserves better than a pile of string replacements. Write the layout in Typst, feed it CSV, JSON, or YAML, and get one PDF per record: certificates, invoices, letters, whatever batch paperwork showed up this time. Python.

**[llmfail](https://github.com/balyakin/llmfail)** — Local proxy that adds failover between LLM providers. Anthropic returning 429s? Falls through to OpenAI or wherever. Mostly just a routing layer, smaller than you'd expect. Go.

**[smartproxy](https://github.com/balyakin/smartproxy)** — Local LLM proxy for the setup that starts with one API key and somehow grows into retry scripts, budget checks, and a cost spreadsheet. Point OpenAI-compatible clients at it and get routing, failover, SQLite telemetry, optional caching, and a terminal dashboard. Go.

**[querygate](https://github.com/balyakin/querygate)** — Go middleware and reverse proxy for the awkward HTTP case where a read needs a request body, but `POST` makes it look like a write. Speaks `QUERY`, advertises `Accept-Query`, caches safe body-aware responses, and can bridge older backends through `POST`. Go.

**[codebone](https://github.com/balyakin/codebone)** — CLI and MCP server for giving agents compact code context. Extracts symbols, signatures, and structure with tree-sitter instead of dumping whole files. TypeScript.

**[ragimg](https://github.com/balyakin/ragimg)** — RAG indexing for the parts of docs that live in images. Reads Markdown/HTML, skips badges and logos, captions useful diagrams/screenshots/charts once, and writes JSONL chunks for the embedding pipeline you already have. Go.

**[skill-eval-runner](https://github.com/balyakin/skill-eval-runner)** — Test runner for `SKILL.md` files. Spins up a fresh workspace, lets an agent work, then checks what actually happened: files, commands, JSON, exit codes, tokens, and CI reports. Built because "the chat looked right" is not a regression test. TypeScript.

**[sqliteq](https://github.com/balyakin/sqliteq)** — Job queues, pub/sub, and scheduled jobs inside a single SQLite file. No daemon, no Redis. Just a file. Rust.

**[SteadySend](https://github.com/balyakin/steady-send)** — File transfer for the dull but painful case: one huge file, a flaky network, and a retry that shouldn't start from zero. If the link drops, run the same command again; it resumes from verified chunks. Go.

**[snapback](https://github.com/balyakin/snapback)** — Incremental local backups for project folders. Per-file deduplication, SQLite index, and restore by date or file when you need to rewind without thinking about it. Python.

**[tokmon](https://github.com/balyakin/tokmon)** — Proxy for tracking token usage and costs across Anthropic/OpenAI. If you run a lot of agents you'll want this before the invoice arrives. Go, SQLite.

**[sudocheck](https://github.com/balyakin/sudocheck)** — Linux privilege escalation audit: sudo rules, SUID/SGID binaries, capabilities, GTFOBins cross-reference. Outputs JSON or SARIF. Go.

**[depshield](https://github.com/balyakin/depshield)** — Supply-chain check for package managers. One command, works across npm/pip/cargo/etc. Go.

**[git-pulse](https://github.com/balyakin/git-pulse)** — Codebase diagnostics from git history: churn, ownership, dead zones. Rust, TUI.

**[TubeSift](https://github.com/balyakin/TubeSift)** — Search YouTube channels by subtitle content, from the terminal. Full-text index. Python, SQLite.

---

## Stack

Go for most backend tooling. Rust when I want small binaries or need the performance. Python for scripting and quick prototypes. SQLite as default storage — you can get surprisingly far without running a server.
