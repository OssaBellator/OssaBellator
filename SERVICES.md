# AI Automation Services

I build bounded AI automation and agent workflows with explicit failure handling, duplicate protection, verification, tests, and operator handoff.

These are example scopes, not a claim that every project fits the same package. Final scope depends on the systems involved and what their APIs/permissions actually allow.

## US$199 — Workflow audit + repair

Best for one existing automation or integration that is unreliable, partially broken, or difficult to maintain.

Typical scope:
- reproduce the current failure;
- inspect data mapping, authentication, API/tool boundaries and current state;
- repair one bounded workflow;
- add basic error/retry handling;
- test a representative success path and one failure path;
- document what changed and how to operate it.

Typical examples:
- webhook -> AI request failing;
- broken API integration;
- duplicate side effects;
- unreliable Claude/MCP tool flow;
- automation that succeeds partially and cannot recover cleanly.

Scope boundary:
- one workflow;
- up to two connected systems;
- no new customer portal or large UI;
- no autonomous financial/payment execution.

## US$399 — New end-to-end automation

Best for one clearly bounded business process.

Typical examples:
- form/questionnaire -> AI analysis -> report/PDF/email;
- webhook -> CRM -> approval -> notification;
- document intake -> extraction -> controlled AI output;
- Claude/MCP tool integration;
- API-to-API workflow.

Includes:
- workflow contract and acceptance criteria;
- implementation;
- up to three integrations/adapters;
- client-editable configuration where appropriate;
- approval boundary for consequential actions;
- idempotency / duplicate protection;
- representative tests;
- verification and recovery behavior;
- run/deployment instructions;
- operator handoff.

## US$699 — Multi-step AI workflow

Best for a larger but still bounded workflow with several steps, branches, or integrations.

Includes everything in the US$399 scope plus:
- up to five integrations/adapters;
- multi-step workflow state;
- partial-failure recovery;
- expanded test matrix;
- CI or automated regression checks where practical;
- architecture and maintenance documentation.

## What I need from you

For most bounded automation projects:

1. one representative input or real workflow example;
2. the business rules / acceptance criteria;
3. the systems/accounts the workflow must connect to;
4. client-owned access or API credentials after the contract starts;
5. which consequential actions may run automatically and which require approval.

Optional inputs:
- brand/report template;
- preferred hosting/runtime;
- existing code/repository;
- representative failure cases.

You do not need to design the technical architecture.

## What I own

I can take responsibility for:
- technical decomposition;
- API/webhook integration;
- TypeScript/Node.js implementation;
- deterministic business rules;
- bounded AI integration;
- approval boundaries;
- retries and idempotency;
- verification;
- tests;
- debugging;
- documentation;
- operator handoff.

## Start with proof

- [Executable business-automation proof](./BUSINESS_AUTOMATION.md)
- [Consolidated business automation case study](https://github.com/OssaBellator/claude-mcp-workflow-audit/blob/main/BUSINESS_AUTOMATION_CASE_STUDY.md)
- [Detailed engineering evidence](./PORTFOLIO.md)

## Boundaries

Production feasibility depends on the selected platforms, their APIs, account permissions and client-owned credentials. I verify those constraints before promising unsupported automation.

The public examples are synthetic portfolio implementations and are not presented as prior paid client deployments.
