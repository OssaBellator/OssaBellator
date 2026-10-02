# OssaBellator

Building practical tooling for bounded, recoverable AI-agent workflows.

## AI coding agent & MCP repository hardening

I maintain an open-source hardening toolkit for repositories using Claude Code, Codex, Cursor, GitHub Actions, MCP servers, hooks, skills, or other agentic development workflows.

The public tools are deliberately bounded: read-only or static evidence first, explicit authority boundaries, no target-code execution unless a workflow specifically requires it, and clear recovery/verification steps.

### Start free

- **Free browser audit:** https://ossabellator.github.io/claude-code-mcp-hardening/free-audit.html
- **Repository security checklist:** https://ossabellator.github.io/claude-code-mcp-hardening/ai-coding-agent-repository-security-checklist.html
- **Open-source toolkit:** https://github.com/OssaBellator/claude-code-mcp-hardening
- **GitHub Action:** `uses: OssaBellator/claude-code-mcp-hardening@v1`

### Fixed-scope help

| Option | Scope |
| --- | --- |
| **A$39 AUD** | Human-reviewed hardening audit for one public GitHub repository |
| **A$79 AUD** | 60-day public-repository watch: baseline, day 30, day 60 |
| **A$149 AUD** | Bounded hands-on audit + implementation/hardening for one workspace |

- **A$39 audit:** https://ossabellator.github.io/claude-code-mcp-hardening/repo-audit.html
- **A$79 watch:** https://ossabellator.github.io/claude-code-mcp-hardening/watch.html
- **A$149 implementation:** https://ossabellator.github.io/claude-code-mcp-hardening/

The paid work is intentionally narrow. It is not penetration testing, incident response, unlimited support, a security certification, or a guarantee that every vulnerability will be found.

## Related workflow-audit toolkit

The earlier workflow-audit project focuses more broadly on MCP integrations, Agent Skills, scheduled automations, side-effect safety, idempotency, partial-failure recovery, and operator handoff:

- **Toolkit:** https://github.com/OssaBellator/claude-mcp-workflow-audit
- **Technical proof:** https://ossabellator.github.io/claude-mcp-workflow-audit/proof.html
- **Agent Skill:** `npx skills add OssaBellator/claude-mcp-workflow-audit --skill auditing-mcp-workflows`

Do not send passwords, API keys, private keys, recovery phrases, production customer data, or other secrets through checkout fields, issues, or proposal messages.
