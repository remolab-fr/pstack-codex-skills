# Adaptation matrix and intentional changes

This distribution preserves the topic and workflow intent of every main skill and playbook while rewriting host-specific behavior. It is not a claim of exact behavioral equivalence.

| Source component | Destination | Treatment |
|---|---|---|
| 51 main skill directories | skills/pstack-*/SKILL.md | Namespaced, rewritten procedures with required shared contract |
| 23 poteto-mode playbooks | workflows/ | Rewritten portable steps with explicit gates and evidence |
| 24 principles | Individual pstack-principle-* skills | Preserve engineering intent; remove scope/authority overreach |
| 3 Benny skills | integrations/benny/procedures/ | Inactive operational references, not ordinary installed skills |
| Benny templates | integrations/benny/templates/ | Secret-free disabled configuration and prompts |
| 2 named agents | roles/ | Host-neutral role profiles |
| 37 supporting reference files | Owning procedure or workflow | Concepts consolidated; host-specific examples are not copied |
| Cursor manifest and custom-mode metadata | Codex adapter and catalog | No runtime registration or settings mutation |
| Model rules and vendor slugs | Abstract roles in adapter | Inherit available host defaults; explicit overrides only |
| Upstream helper scripts/tests/dependency files | No executable counterpart | Excluded; runtime behavior is not reproduced |
| Repository development tooling | scripts/check and CI | Authored separately to validate packaging and content; does not execute skill workflows |
| Documentation artwork | None | Omitted as nonessential to procedural source |
| Upstream guides | README, catalog and adaptation notes | Rewritten for repository-source use |
| MIT notice | LICENSE, NOTICE and each skill license | Preserved |

The exact per-file output or omission reason is recorded in [source-inventory.json](../provenance/source-inventory.json).

## Required behavioral differences

- Unconditional reversible/external action authority becomes explicit scope and host permission checks
- Cursor Task/subagent types, model rules, slash commands and custom modes become abstract operations
- Protected transcript filesystem discovery becomes supported scoped history retrieval
- An investigation does not automatically turn into code, a PR or a new skill edit
- PR status, drive-to-ready and shipping remain distinct; merge requires explicit scope
- Comment review preserves required notices and uncertain safety constraints
- Cleanup does not consider untracked content disposable or a closed PR proof of merger
- Dependency bootstraps do not run when reading or invoking a text skill
- Webhook configuration uses only supported secure provider paths; no credential-file copying or VPN install
- Benny requires actual credential/tool isolation for isolation-dependent execution
- Failed tracker handoffs use only authorized reversible compensation, never assumed permanent deletion
- Logs hold concise decisions and observable evidence, not private reasoning

## Runtime exclusions
The upstream bootstrap can install dependencies and restart commands. Its PR watcher assumes a GitHub CLI adapter. Its orchestration store can invoke Graphite. Its worktree audit changes local refs, assumes origin/main, inspects Cursor transcripts and contains platform-specific commands. None is shipped or run here.

The original package declares commander 14.0.0, with development dependency ranges bun-types latest and typescript latest. The pinned upstream lockfile resolved these to bun-types 1.3.14 and typescript 7.0.2. These are source-audit facts, not dependencies of this text-only distribution.

## Validation boundary
Static checks establish packaging, links, counts and obvious forbidden dependencies. They do not demonstrate external provider access, execution environment isolation, workflow runtime behavior or successful personal installation. Any live integration requires its own authorized setup and proof.

## Codex portability review (2026-10-07)

The second content review distinguishes removal of runtime dependencies from preservation of useful workflow semantics. The source-only port does not depend on Cursor registration, model aliases, tools, transcript storage, custom modes or helper execution. Source URLs and inventory paths retain upstream names for traceability; they are attribution, not runtime imports.

The adapter now separates local Codex CLI/IDE execution, Codex Cloud tasks and hosted-assistant tools. Standard Codex does not require a hosted user-message, history-search or task-creation API. Local skill discovery uses documented paths; symlinked entries resolve resources from their physical checkout. Copying one skill directory alone is unsupported because contracts, workflows and related skills are shared.

The review also checks host-neutral safeguards that were over-compressed in the initial rewrite: exact-revision evidence, independent reviews, shared-writer ownership, controlled experiments, explicit failure and recovery paths, and safe source-thread handoffs. These are procedural instructions for an available host, not reimplemented upstream executables. Live integration, isolation and automatic skill selection remain separate validation work.
