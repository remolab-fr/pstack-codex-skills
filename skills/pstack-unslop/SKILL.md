---
name: pstack-unslop
description: "Use when the user requests unslop or its workflow. Rewrite the requested prose to remove filler, unsupported claims, decorative structure and vague abstractions while preserving meaning, uncertainty, required terminology and audience."
---

# Unslop

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- source.read (as needed)
- artifacts.write (only when saving is requested)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The requested artifact or change, relevant source/revisions, acceptance criteria, constraints and authorized output destination.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Follow explicit user style and host message formatting first. Do not turn an on-demand editing workflow into a permanent global style override.
2. Scan concretely for vague attributions, generic conclusions, filler, inflated verbs, forced symmetry, unnecessary contrast framing, decorative headings, synonym cycling, and metaphors that hide the mechanism. Replace unsupported intensity with a source or measured fact. Rewrite the requested prose to remove filler, unsupported claims, decorative structure and vague abstractions while preserving meaning, uncertainty, required terminology and audience.
3. Keep one stable name per concept and prefer complete, active sentences. Split dense clauses but restore articles and verbs when compression makes the reader decode fragments. Preserve evidence-backed uncertainty; do not turn cautious claims into certainty for style.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Source

Adapted from [pstack/skills/unslop/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/unslop/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
