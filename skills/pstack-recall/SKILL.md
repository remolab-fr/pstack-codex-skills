---
name: pstack-recall
description: "Use when the user requests recall or its workflow. Use a supplied current-state capsule when sufficient."
---

# Recall

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- history.search or supplied task evidence
- source.read
- artifacts.write (approved persistent changes only)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The question or topic, known source anchors, relevant time window and available authorized evidence sources.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Use a supplied current-state capsule when sufficient.
2. Never enumerate private session directories. Keep private context out of public artifacts.
3. Otherwise scope the topic, time window and workspace, then query the host's authorized history/context interface. Use an explicit topic, workspace, and time window; do not silently shrink all-history requests into a recent sample. For a named feature or bug, inspect the relevant shared record as well as authorized conversation history, including recurring reports and previously reverted fixes.
4. Resolve relevant PRs, branches, tickets and shared-record evidence and verify their current state before reporting.
5. Tag each thread with verified current status such as merged, open PR, in flight, verified but uncommitted, reverted, or planned. Keep the capsule and recurring-problem list short without dropping an entire in-scope thread; finish with the single most useful next move. State evidence-source gaps. Return a concise capsule, per-thread status, important recurring problems and the next concrete move.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-why](../pstack-why/SKILL.md)

## Source

Adapted from [pstack/skills/recall/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/recall/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
