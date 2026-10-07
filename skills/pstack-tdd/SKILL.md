---
name: pstack-tdd
description: "Use when the user requests tdd or its workflow. Use when explicitly requested or when a practical local regression test is clear."
---

# Tdd

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

1. Use when explicitly requested or when a practical local regression test is clear. Identify intended behavior and the smallest discriminating reproduction. Avoid implementation-mirroring tests and elaborate new infrastructure for a small bug.
2. Write a behavioral test without weakening existing assertions to accommodate an incorrect implementation. Run it before the fix and confirm the failure is the intended defect, not a setup error; repair the test setup first if needed. Make flaky reproduction deterministic where practical and name the signal locked down. Then make the minimal authorized fix and rerun the test and relevant nearby checks.
3. If a failing test is impractical, explain why and provide the strongest available reproducible evidence.
4. Report the failing-before check and actual failure, passing-after run, and relevant nearby validation. If the before state could not be demonstrated, say so plainly rather than claiming red/green evidence.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-principle-test-behavior-not-implementation](../pstack-principle-test-behavior-not-implementation/SKILL.md)

## Source

Adapted from [pstack/skills/tdd/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/tdd/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
