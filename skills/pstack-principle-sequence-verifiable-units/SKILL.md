---
name: pstack-principle-sequence-verifiable-units
description: "Apply the sequence verifiable units principle when reviewing or implementing an explicitly scoped engineering task. Break a multi-step effort into units with observable acceptance checks and explicit dependencies."
---

# Principle Sequence Verifiable Units

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

1. Break a multi-step effort into units with observable acceptance checks and explicit dependencies. Verify each delivered unit and preserve evidence before moving the frontier. For each unit bracket one change with a known baseline and a specific after-check; do not accumulate unchecked changes. When commits or PRs are authorized, order them to demonstrate the argument, such as failing reproduction then fix, baseline then treatment, or subtraction then redesign. Do not rebase or mutate branches without applicable authority.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Source

Adapted from [pstack/skills/principle-sequence-verifiable-units/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/principle-sequence-verifiable-units/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
