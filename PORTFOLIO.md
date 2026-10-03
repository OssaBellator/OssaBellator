# Engineering Evidence Portfolio

This page is a technical review shortcut for the projects pinned on my GitHub profile. It focuses on **problem framing, architecture decisions, inspectable implementation, verification surfaces, and explicit limitations** rather than broad capability claims.

Repository counts below describe the current `main` tree structure. A test-file count is evidence of test surface, not a claim that every test passes on every operating system or environment.

## 1. Claude Code & MCP Workspace Hardening

**Problem.** AI-assisted repositories accumulate MCP configuration, instructions, hooks, CI permissions and credential surfaces faster than teams can reason about them.

**Design.** Start read-only. Inventory repository-visible agent/tool surfaces without executing target code, then separate evidence collection from human review and any later remediation.

**Inspect.**

- [Repository](https://github.com/OssaBellator/claude-code-mcp-hardening)
- [Scanner entry point](https://github.com/OssaBellator/claude-code-mcp-hardening/blob/main/audit.mjs)
- [Shared audit logic](https://github.com/OssaBellator/claude-code-mcp-hardening/blob/main/audit-lib.mjs)
- [Regression test](https://github.com/OssaBellator/claude-code-mcp-hardening/blob/main/test-audit.mjs)
- [Self-audit workflow](https://github.com/OssaBellator/claude-code-mcp-hardening/blob/main/.github/workflows/self-audit.yml)

**Current evidence surface.** 43 tracked files, 2 test files and 2 GitHub workflow files on `main`.

**Boundary.** Inventory findings are review signals, not penetration-test findings or vulnerability certification.

---

## 2. Bounded Computer-Use Runtime

**Problem.** Computer-use systems often treat transport success as task success and then retry through stale targets or ambiguous side effects.

**Design.** Make target freshness, effect authority, dispatch state and post-action verification separate concepts. Preserve uncertainty rather than converting it into a retry-safe failure.

**Inspect.**

- [Repository](https://github.com/OssaBellator/computer-use)
- [Case study](https://github.com/OssaBellator/computer-use/blob/main/CASE_STUDY.md)
- [Neutral environment contract](https://github.com/OssaBellator/computer-use/blob/main/src/computer/environmentAdapter.ts)
- [Cross-adapter task runtime](https://github.com/OssaBellator/computer-use/blob/main/src/computer/computerTaskRuntime.ts)
- [Architecture](https://github.com/OssaBellator/computer-use/blob/main/docs/computer-use-architecture.md)
- [Task-runtime tests](https://github.com/OssaBellator/computer-use/blob/main/tests/computerTaskRuntime.test.ts)
- [Standalone Chromium integration smoke](https://github.com/OssaBellator/computer-use/blob/main/tests/integration/standaloneChromiumSmoke.test.mjs)

**Current evidence surface.** 383 tracked files, 211 test files and 40 architecture/design documents on `main`.

**Boundary.** Chromium is the strongest end-to-end implementation. Several other environment adapters are neutral foundations or reference implementations rather than uniformly production-validated platform backends.

---

## 3. FileOp

**Problem.** Fast Windows file tools often split indexing, storage analysis and mutation into different authority models, creating stale decisions and weak recovery boundaries.

**Design.** One reusable NTFS/USN-backed index feeds Search, Files and Storage. Evidence remains non-authorizing; destructive actions require fresh identity/path validation, explicit authorization and durable history.

**Inspect.**

- [Repository](https://github.com/OssaBellator/fileop)
- [Case study](https://github.com/OssaBellator/fileop/blob/main/CASE_STUDY.md)
- [Architecture](https://github.com/OssaBellator/fileop/blob/main/docs/architecture.md)
- [Files execution boundary](https://github.com/OssaBellator/fileop/blob/main/docs/files-browser.md)
- [NTFS synchronizer](https://github.com/OssaBellator/fileop/blob/main/src/FileOp.Windows/Ntfs/NtfsIndexSynchronizer.cs)
- [Helper trust policy](https://github.com/OssaBellator/fileop/blob/main/src/FileOp.Windows/IndexingService/IndexingServiceHelperTrustPolicy.cs)
- [Representative delete validation tests](https://github.com/OssaBellator/fileop/blob/main/tests/FileOp.Windows.Tests/FileDeleteOperationExecutionValidationTests.cs)
- [Local validation contract](https://github.com/OssaBellator/fileop/blob/main/docs/local-validation.md)

**Current evidence surface.** 702 tracked files, 173 test files and 88 focused design/operations documents on `main`.

**Boundary.** The repository documents a production signing/package gate that still requires a real production-certificate dry run before calling a release production-ready.

---

## 4. Unified Project Manager

**Problem.** npm/pnpm/Yarn/Bun, Python managers, Cargo, Go and .NET each have different ownership, lock, graph, cache and mutation semantics. Flattening them into one fake universal resolver loses important evidence.

**Design.** Keep native tools authoritative. Normalize observations and policy while preserving ecosystem-specific uncertainty. Preview before mutation or network access, then persist bounded mutation evidence.

**Inspect.**

- [Repository](https://github.com/OssaBellator/Unified-Project-Manager)
- [Architecture](https://github.com/OssaBellator/Unified-Project-Manager/blob/main/docs/ARCHITECTURE.md)
- [Package-operation provider contract](https://github.com/OssaBellator/Unified-Project-Manager/blob/main/docs/PACKAGE_OPERATION_PROVIDER_CONTRACT.md)
- [Mutation receipts](https://github.com/OssaBellator/Unified-Project-Manager/blob/main/docs/MUTATION_RECEIPTS.md)
- [Provider registry](https://github.com/OssaBellator/Unified-Project-Manager/blob/main/src/unified_project_manager/provider_registry.py)
- [Native-security regression driver](https://github.com/OssaBellator/Unified-Project-Manager/blob/main/scripts/test-native-security.sh)

**Current evidence surface.** 475 tracked files, 237 test files and 38 focused documents on `main`. Validation is intentionally local/script-driven rather than GitHub Actions.

**Boundary.** Receipt chains are tamper-evident but not externally authenticated. Conditional or ambiguous dependency evidence is retained as such instead of silently upgraded to certainty.

---

## 5. E2H — Evidence-to-Harness

**Problem.** AI-agent evaluations can become difficult to reproduce when success depends on opaque transcripts, mutable workspaces or unverifiable state.

**Design.** Turn observable events and artifacts into versioned capsules, content-addressed evidence, mutation-verified harnesses, snapshots, controlled experiments and verifiable release artifacts.

**Inspect.**

- [Repository](https://github.com/OssaBellator/E2H)
- [Case study](https://github.com/OssaBellator/E2H/blob/main/CASE_STUDY.md)
- [Workspace snapshots](https://github.com/OssaBellator/E2H/blob/main/src/e2h/workspace_snapshot.py)
- [Runtime request planning](https://github.com/OssaBellator/E2H/blob/main/src/e2h/runtime_plan.py)
- [Release integrity](https://github.com/OssaBellator/E2H/blob/main/docs/release-integrity.md)
- [Provider conformance](https://github.com/OssaBellator/E2H/blob/main/docs/provider-runtime-conformance.md)
- [Compiler boundary tests](https://github.com/OssaBellator/E2H/blob/main/tests/test_compiler_boundaries.py)
- [Release-integrity workflow](https://github.com/OssaBellator/E2H/blob/main/.github/workflows/release-integrity.yml)

**Current evidence surface.** 517 tracked files, 338 test files, 20 focused documents and 10 GitHub workflow files on `main`. CI exercises Python 3.11, 3.12 and 3.13.

**Boundary.** A valid capsule or release artifact proves defined evidence relationships; it is not a general-purpose security sandbox and does not establish that arbitrary candidate code is safe.

---

## What these projects are meant to demonstrate

Across the five projects, the recurring engineering themes are:

- explicit authority rather than ambient permission;
- read/observe before mutate;
- stale-target and identity revalidation;
- uncertainty preserved across failures;
- dispatch separated from verification;
- durable evidence and recovery paths;
- deterministic or bounded validation where practical;
- limitations documented alongside implemented capability.

For contract work, see my [GitHub profile](https://github.com/OssaBellator) or [Upwork profile](https://www.upwork.com/freelancers/~01fa363b7b5fea3801).
