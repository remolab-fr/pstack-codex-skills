---
name: pstack-principle-separate-before-serializing-shared-state
description: "Apply the separate before serializing shared state principle when reviewing or implementing an explicitly scoped engineering task. Give parallel workers separate writable outputs and clear ownership."
---

# Principle Separate Before Serializing Shared State

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

1. Give parallel workers separate writable outputs and clear ownership. Use serialization only when one shared writer or resource is a real invariant. Inventory files, branches, keys, and state objects with multiple writers. Distinct fields inside one rewritten JSON file are still shared mutation. Use separate owned objects and merge at a read/report boundary when possible; otherwise enforce one-writer access with an actual lock, sequential phase, or atomic compare-and-swap.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Source

Adapted from [pstack/skills/principle-separate-before-serializing-shared-state/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/principle-separate-before-serializing-shared-state/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
