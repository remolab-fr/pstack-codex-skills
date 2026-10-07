---
name: pstack-architect
description: "Use when the user requests architect or its workflow. Ground the requested change in existing behavior and constraints."
---

# Architect

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

1. Ground existing runtime paths with [pstack-how](../pstack-how/SKILL.md); when ownership or layering changes, use [pstack-why](../pstack-why/SKILL.md) to turn historical rationale into design constraints. Skip this only for genuinely isolated greenfield work.
2. Write the caller experience first: imports, two or three realistic calls, and returned values. Derive the types and signatures from that usage. For non-obvious design work, compare at least two structurally different sketches before selecting a base. Sketch the smallest viable types, signatures, module boundaries and ownership before implementation.
3. For a consequential design choice, compare independent sketches in isolated outputs using [pstack-arena](../pstack-arena/SKILL.md). Screen designs for a wide interface hiding little complexity, exposed transport/storage details, modules split only by execution phase, empty forwarding layers, shared writers, duplicate supported paths, importable internals, and manually synchronized lists. Prefer one clear owner and a small interface that hides substantial behavior.
4. Keep a rationale beside the sketch: problem, caller usage, chosen shape and invariants, synthesis decision, accepted tradeoffs, concrete alternatives, open risks, and first implementation step. A prototype is not a finished implementation. Present unresolved product choices; obtain approval where required.
5. Implement against the selected sketch and verify observable behavior. Track implementation deviations. Repeated same-shaped workarounds, unsafe casts, unexplained shared-state locks, or callers depending on internals indicate a design problem. Re-ground and compare revised shapes rather than accumulating patches; one isolated edge case need not invalidate the whole design. If new facts invalidate the design, revise the sketch rather than adding compatibility layers by reflex.
6. Return the chosen shape, rejected alternatives and evidence.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-how](../pstack-how/SKILL.md)
- [pstack-arena](../pstack-arena/SKILL.md)

## Source

Adapted from [pstack/skills/architect/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/architect/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
