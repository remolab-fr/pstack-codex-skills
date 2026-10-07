---
name: pstack-show-me-your-work
description: "Use when the user requests show me your work or its workflow. Maintain a concise outcome/evidence record for a long or unattended task: timestamp, phase, decision summary, public rationale, evidence reference and result."
---

# Show Me Your Work

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- source.read
- source.compare (when relevant)
- delegation (optional)
- execution.run (proof only when authorized)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The question or topic, known source anchors, relevant time window and available authorized evidence sources.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Exclude secrets, private internal deliberation and unrelated conversation content. Prefer an append-only local artifact scoped to the task; publishing or committing the log requires appropriate authority and review.
2. Use one canonical TSV or equivalent structured log with single-line timestamp, phase, decision, public rationale, evidence pointer, and result fields. Log meaningful forks, unit checks, pivots, reverts, blockers, and iteration outcomes rather than every tool action. Neutralize formula-leading spreadsheet cells.
3. Preserve append-only history. When resuming a shared log, inspect its tail and delimit this run’s entries with a start record identifying intervening rows and this run. Do not attribute another run’s claims to the current run. Record assumptions and superseding corrections.
4. Audit claims against available tool results and artifacts, not inaccessible session files. Before handoff, resolve each of this run’s evidence pointers against authorized tool results and artifacts. Add missing consequential decisions and superseding corrections rather than rewriting the old story.
5. When an independent reviewer is available, have it inspect the trail and available execution evidence for weak claims, skipped verification, and risky choices. Prefer a different model family only when available and permitted; otherwise disclose the limitation. Report concise attention flags with row references, including no flags when justified.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-principle-prove-it-works](../pstack-principle-prove-it-works/SKILL.md)

## Source

Adapted from [pstack/skills/show-me-your-work/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/show-me-your-work/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
