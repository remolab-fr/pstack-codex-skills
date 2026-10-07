---
name: pstack-arena
description: "Use when the user requests arena or its workflow. Define the artifact and a task-specific rubric with 3–6 checkable criteria."
---

# Arena

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- source.read
- execution.run (when needed and authorized)
- artifacts.write (within scope)
- delegation (optional)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The requested artifact or change, relevant source/revisions, acceptance criteria, constraints and authorized output destination.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Define the artifact and a task-specific rubric with three to six checkable criteria. Keep the brief neutral about the preferred answer.
2. When independent workers are available, give each the same task, grounding, and isolated writable output. Otherwise produce sequential alternative drafts and label this a single-agent comparison with no independent validation. Use different models only when available and permitted.
3. Collect each candidate artifact and its short rationale naming rejected alternatives. Wait until candidates stop writing, then read every finished artifact end to end. Record missing candidates as dropouts.
4. If an independent judge is available, give it the finished candidates by path label and the rubric for read-only critique. Otherwise perform and disclose self-review. Independent runs on one model are not cross-model validation.
5. Score candidates criterion by criterion. If a judge ran, compare its rationale with the lead’s and resolve disagreements on evidence. Prefer the base maintainers can extend without breaking invariants, with smaller clearer interfaces when other criteria tie.
6. Revisit losing candidates and adapt only improvements that fit the chosen design. Record the base, each graft and its origin, rejected ideas, and dropouts. Convergence needs no artificial graft; incompatible divergent shapes call for a clearer brief rather than averaging designs.
7. Verify the synthesized artifact. If it fails, distinguish a defective brief from a useful candidate idea overlooked during integration and correct the relevant stage rather than patching around the failed check.
8. Return the artifact and concise synthesis record, including actual model diversity, whether an independent judge ran, tradeoffs, disagreements, and verification evidence.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-interrogate](../pstack-interrogate/SKILL.md)
- [pstack-principle-separate-before-serializing-shared-state](../pstack-principle-separate-before-serializing-shared-state/SKILL.md)

## Source

Adapted from [pstack/skills/arena/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/arena/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
