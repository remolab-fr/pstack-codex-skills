---
name: pstack-principle-test-behavior-not-implementation
description: "Apply the test behavior not implementation principle when reviewing or implementing an explicitly scoped engineering task. Exercise the interface used by real callers and assert meaningful expected results."
---

# Principle Test Behavior Not Implementation

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- source.read (when inspecting a change)
- execution.run (only for authorized verification)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The scoped decision or change, existing invariants, affected consumers, and available evidence.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Exercise the interface used by real callers and assert meaningful expected results. A test must fail when the behavior is broken, rather than merely mirror implementation or mocks. Audit whether the test would detect an empty or no-op subject. Avoid expectations calculated by the subject, fixture-only assertions, incidental call counts, and constant restatements. Assert concrete output or meaningful effects; pair absence cases with a positive case when needed. Keep meaningful schema/table relationships and compile-time contracts.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Source

Adapted from [pstack/skills/principle-test-behavior-not-implementation/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/principle-test-behavior-not-implementation/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
