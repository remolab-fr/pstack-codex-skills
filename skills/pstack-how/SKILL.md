---
name: pstack-how
description: "Use when the user requests how or its workflow. For a narrow question, inspect the relevant source and explain it directly."
---

# How

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

1. Do not edit code just to answer how it works.
2. For a narrow question, inspect the relevant source and explain it directly. For a subsystem, partition read-only exploration by ownership or runtime path, then synthesize one coherent explanation.
3. Trace one real trigger through the actual implementation, showing transformed data at each step, key types, ownership, and inputs/outputs across module boundaries. Names and directory lists are not a runtime explanation. For a larger subsystem, give readers distinct exploration slices and require components, traced flow, files read, boundaries, surprises, and unresolved links. Synthesize overview, concepts, flow, where things live, and gotchas as applicable; never invent a connection that could not be traced.
4. Name the data shape, entry points, ownership boundaries and observable execution flow. Cite source locations and distinguish verified behavior from inference.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Source

Adapted from [pstack/skills/how/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/how/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
