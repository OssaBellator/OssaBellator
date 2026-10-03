# OssaBellator

Building bounded, recoverable AI-agent infrastructure — with an emphasis on **Claude Code / MCP hardening, computer-use safety, automation reliability, and verifiable side effects**.

## Featured work

| Project | What it demonstrates |
| --- | --- |
| **[claude-code-mcp-hardening](https://github.com/OssaBellator/claude-code-mcp-hardening)** | Practical repository hardening for Claude Code, Codex, Cursor, MCP servers, hooks, skills, and GitHub Actions. Includes a deterministic scanner, GitHub Action, Agent Skill, security checklist, and fixed-scope human review. |
| **[computer-use](https://github.com/OssaBellator/computer-use)** | Reference architecture for bounded computer-use runtimes: generation-aware targets, approval boundaries, dispatch uncertainty, verification, checkpoints, browser/CDP interaction, and multi-adapter computer contracts. This work became a reference input for Minimal MCP. |
| **[claude-mcp-workflow-audit](https://github.com/OssaBellator/claude-mcp-workflow-audit)** | Earlier workflow-audit toolkit covering MCP integrations, Agent Skills, scheduled automation, idempotency, partial-failure recovery, and operator handoff. |

## Other public engineering work

| Project | Focus |
| --- | --- |
| **[E2H](https://github.com/OssaBellator/E2H)** | Evidence-to-harness infrastructure for reproducible AI-agent evaluation, deterministic replay, observable traces, and verifiable releases. |
| **[UCOF](https://github.com/OssaBellator/UCOF)** | Rust research implementation of a bounded, self-describing, chunk-addressable container format with integrity, recovery, partial access, and fuzzing. |
| **[Lumina PDF Studio](https://github.com/OssaBellator/Lumina-PDF-Studio)** | Local-first PDF workspace with source-preserving edits, document analysis, OCR options, and review-gated AI changes. |
| **[No-Three-in-Line Research](https://github.com/OssaBellator/no-three-in-line-research)** | Computational mathematics notebook that separates proved results, conditional reductions, heuristics, refutations, and verification scripts. |

## What I work on

- **AI-agent & MCP architecture** — tool boundaries, permissions, credentials, retries, recovery, and verification.
- **Claude Code / coding-agent workflows** — repository instructions, hooks, skills, CI authority, and bounded automation.
- **Computer-use systems** — semantic-first interaction, target freshness, guarded native input, side-effect verification, and conservative retry behavior.
- **TypeScript / Node.js automation** — APIs, workflow orchestration, developer tooling, and failure-safe integrations.
- **QA & automation reliability** — testable acceptance criteria, Windows/CI automation boundaries, and evidence-driven handoff.

## Start with the open-source tools

- **Free public-repo audit:** https://ossabellator.github.io/claude-code-mcp-hardening/free-audit.html
- **Repository security checklist:** https://ossabellator.github.io/claude-code-mcp-hardening/ai-coding-agent-repository-security-checklist.html
- **GitHub Action:** `uses: OssaBellator/claude-code-mcp-hardening@v1`
- **Agent Skill:** `npx skills add OssaBellator/claude-code-mcp-hardening --skill auditing-ai-agent-repositories`

## Fixed-scope help

For teams that want a human review or implementation pass, I offer deliberately bounded engagements rather than open-ended “AI transformation” work:

- **A$39 AUD** — human-reviewed hardening audit for one public GitHub repository
- **A$79 AUD** — 60-day public-repository watch (baseline, day 30, day 60)
- **A$149 AUD** — bounded hands-on audit + implementation/hardening for one workspace

Details: https://ossabellator.github.io/claude-code-mcp-hardening/

## Engineering stance

I prefer systems that make authority explicit, preserve uncertainty instead of guessing, separate dispatch from verification, and leave a clear recovery path.

The public repositories are designed around bounded evidence and reproducible behavior. They do **not** claim penetration-test coverage, vulnerability certification, or permission to perform consequential actions without the appropriate operator approval.

Please do not send passwords, API keys, private keys, recovery phrases, production customer data, or other secrets through issues, checkout fields, or proposal messages.
