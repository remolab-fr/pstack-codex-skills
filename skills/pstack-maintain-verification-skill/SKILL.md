---
name: pstack-maintain-verification-skill
description: "Use when the user requests maintain verification skill or its workflow. Locate the requested verification skill and read every feature-map entry."
---

# Maintain Verification Skill

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

The requested configuration or procedure, its intended scope and destination, existing user-owned material, and evidence of what the host can actually support.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Locate the requested verification skill and read every feature-map entry. If no target exists, report that; if several plausible targets remain, resolve which one before editing. Reconcile the feature index with actual feature files, then review recent source changes for missing user-facing features backed by concrete paths.
2. Edit only the approved verification materials; report product bugs separately. A request for one audit does not create a recurring schedule.
3. Partition read-only source review per feature. Obtain a source summary and a concise live recipe for every feature. Combine overlapping recipes to reduce setup; plan live coverage of every feature even when source review found no drift. Missing source or live coverage prevents a clean outcome.
4. Run doctor before the first drive, on every fresh session, and after surprising or failed behavior. If the process is healthy but the UI is stuck, reset or relaunch to a known state. Repair confirmed doctor/harness drift within the approved scope and retry, restarting only what the repair invalidates. One coordinator or isolated authorized executor drives the live surface, health-checking unexpected states and retaining evidence through cleanup. Clean failed-iteration residue and owned processes throughout the run; preserve earlier evidence after every cleanup. Record an unreachable feature only with the attempted route and concrete missing prerequisite, such as authentication, entitlement, OS, or external state.
5. Distinguish documentation drift, harness gaps and product regressions. Re-drive every changed harness recipe live before calling it proven. Final teardown occurs after all re-proofs. Report a per-feature source/live coverage ledger, confirmed drift, product defects, unreachable prerequisites, retained evidence, and clean/changed/blocked. A product regression must not be rewritten as expected behavior.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-create-verification-skill](../pstack-create-verification-skill/SKILL.md)

## Source

Adapted from [pstack/skills/maintain-verification-skill/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/maintain-verification-skill/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
