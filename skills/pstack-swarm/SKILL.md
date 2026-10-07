---
name: pstack-swarm
description: "Use when the user requests swarm or its workflow. Define the done predicate and choose partitioned coverage, independent races or a mixed shape."
---

# Swarm

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

1. Define the done predicate and choose partitioned coverage, independent races or a mixed shape. State whether selection is first-pass, rank-all or best-of.
2. Each standalone brief states goal, scope, slice or race arm, exact revisions, acceptance method, and report contract. Return PASS, ISSUES, or BLOCKED with evidence and all proven issues. Isolate writable outputs, name exact source revisions and measurement protocols, and collect every required slice.
3. Queue work within actual host capacity; the requested worker count need not equal concurrent workers. Reuse or replace workers according to the host lifecycle contract.
4. Reject a result that omits the required revision or measurement protocol, request one corrected attempt, and record an explicit gap if it still fails. A dropout or missing coverage slice cannot become a pass. Apply the declared race selection rule and report any unfinished arms honestly. Aggregate failures and disagreements rather than hiding them.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-arena](../pstack-arena/SKILL.md)

## Source

Adapted from [pstack/skills/swarm/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/swarm/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
