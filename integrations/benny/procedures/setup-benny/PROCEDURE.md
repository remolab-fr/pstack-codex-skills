# Setup Benny

Operational reference procedure. Loading this file does not create or enable an automation.

## Before starting

Read the [portable execution contract](../../../../core/contract.md). Resolve host operations through the [Codex adapter](../../../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Inputs

Verified source channel/thread, authorized sender and repository, configured tracker/control adapter, safe test environment, bounded budgets and granted actions.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure
1. Prepare disabled, secret-free configuration naming source channel, trusted triage identity, repository/revision, tracker destinations and actions, routing map, control adapter, completed feature map, budgets and permitted outputs. Fail setup for ambiguous required fields.
2. Keep user configuration outside distributed procedures and preserve local changes. Use stable paths that a fresh authorized run can actually read; verify persistence and required procedure/skill availability rather than assuming the current session represents deployment.
3. Verify read and write capabilities separately, including source-thread reads/replies, attachment access, tracker search/read/create/update and reversible compensation, repository/history access and draft-PR creation. Do not infer a write grant from a connected tool.
4. Require actual credential and tool isolation for isolation-dependent execution. Keep secrets outside files and prompts. Do not substitute an equally privileged coordinator when the required boundary is absent.
5. Validate the feature map and control adapter: launch the exact app/revision safely, identify it, navigate real user paths, reset disposable state, inspect read-only state, capture screenshots/recordings and clean up. Run an authorized harmless smoke test through these capabilities before enabling reproduction.
6. Keep owner pings off unless configured and authorized; never infer a routing destination or owner from superficial symptoms.
7. Prepare two disabled plans with supported triggers and stable references: triage one source report, then reproduce only after its trusted triage result. Distinguish new creation from updating an existing automation to avoid duplicates. Obtain exact scope, destination and recurring-work authorization before configuring live work.
8. Before normal traffic, run an authorized thread-safety test: one verdict under immutable source coordinates, exactly one configured marker, trusted-identity acceptance, no source-channel root/fallback posts, no worker Slack writes, and no writes when coordinates, parent or preflight are missing. Enable only after the test and control smoke check pass; otherwise report the precise blocker.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Source

Adapted from [pstack/automations/benny/skills/setup-benny/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/automations/benny/skills/setup-benny/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [repository LICENSE](../../../../LICENSE).
