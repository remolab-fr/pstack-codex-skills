---
name: pstack-correct
description: "Use when the user requests correct or its workflow. Identify a supported recurring mistake from the scoped task evidence."
---

# Correct

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

1. Make only authorized in-scope edits; a correction does not authorize modifying unrelated skills or settings. Identify a supported recurring mistake from the scoped task evidence. Group scoped commits, reverts, review comments, and corrections into mistake classes. Treat repeated evidence as a class, prioritize frequent classes, and record why the next stronger enforcement layer is unsuitable.
2. Prefer eliminating the invalid path through architecture, then types, then a narrow lint or CI check, then a behavioral regression test. When introducing a check to a codebase with existing violations, consider preventing new violations without blocking unrelated work. Make its error name the supported replacement. Use the same check locally and in CI when that configuration change is authorized. Use prose for judgment that cannot be enforced.
3. Demonstrate that the proposed safeguard detects a real past failure and does not reject valid behavior.
4. Keep an authorized rule-to-enforcement mapping where maintainers expect it. Remove redundant prose only after its structural replacement is demonstrated; exceptions need a reason, bounded lifetime, and appropriate approval.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-principle-encode-lessons-in-structure](../pstack-principle-encode-lessons-in-structure/SKILL.md)
- [pstack-tdd](../pstack-tdd/SKILL.md)

## Source

Adapted from [pstack/skills/correct/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/correct/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
