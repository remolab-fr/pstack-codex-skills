---
name: pstack-poteto-mode
description: "Use when the user requests poteto mode or its workflow. Route the requested outcome to the narrowest workflow below."
---

# Poteto Mode

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

1. Route the requested outcome to the narrowest workflow below.
2. Read only the relevant procedures and principles.
3. Define scope, permissions, capabilities, inputs, evidence and a done predicate before mutation.
4. Understand behavior before changing it; compare consequential design alternatives; name ownership and data shapes; implement in isolated verifiable units.
5. Delegate independent work through the selected host adapter and keep one writer per shared artifact.
6. Verify the real result, explain remaining uncertainty and stop at the user's completion condition.
7. This workflow does not override host policies, conversation style or approval requirements, and does not automatically open a pull request, start a schedule, publish, install software or merge.

## Workflow index

Choose the narrowest relevant workflow. Read it before acting.
- [investigation](../../workflows/investigation.md)
- [bug-fix](../../workflows/bug-fix.md)
- [perf-issue](../../workflows/perf-issue.md)
- [hillclimb](../../workflows/hillclimb.md)
- [runtime-forensics](../../workflows/runtime-forensics.md)
- [trace-forensics](../../workflows/trace-forensics.md)
- [feature](../../workflows/feature.md)
- [refactoring](../../workflows/refactoring.md)
- [prototype](../../workflows/prototype.md)
- [visual-parity](../../workflows/visual-parity.md)
- [authoring-a-skill](../../workflows/authoring-a-skill.md)
- [eval](../../workflows/eval.md)
- [babysit](../../workflows/babysit.md)
- [shipping](../../workflows/shipping.md)
- [autonomous-run](../../workflows/autonomous-run.md)
- [orchestrate](../../workflows/orchestrate.md)
- [autopilot-full](../../workflows/autopilot-full.md)
- [autopilot-stack](../../workflows/autopilot-stack.md)
- [session-pickup](../../workflows/session-pickup.md)
- [pause-safely](../../workflows/pause-safely.md)
- [multi-phase-plan](../../workflows/multi-phase-plan.md)
- [worktree-cleanup](../../workflows/worktree-cleanup.md)
- [opening-a-pr](../../workflows/opening-a-pr.md)

## Principle index

Read the specific principle before applying it.
- [pstack-principle-attack-the-premise](../pstack-principle-attack-the-premise/SKILL.md)
- [pstack-principle-boundary-discipline](../pstack-principle-boundary-discipline/SKILL.md)
- [pstack-principle-build-the-lever](../pstack-principle-build-the-lever/SKILL.md)
- [pstack-principle-encode-lessons-in-structure](../pstack-principle-encode-lessons-in-structure/SKILL.md)
- [pstack-principle-exhaust-the-design-space](../pstack-principle-exhaust-the-design-space/SKILL.md)
- [pstack-principle-experience-first](../pstack-principle-experience-first/SKILL.md)
- [pstack-principle-explain-the-number](../pstack-principle-explain-the-number/SKILL.md)
- [pstack-principle-fix-root-causes](../pstack-principle-fix-root-causes/SKILL.md)
- [pstack-principle-foundational-thinking](../pstack-principle-foundational-thinking/SKILL.md)
- [pstack-principle-guard-the-context-window](../pstack-principle-guard-the-context-window/SKILL.md)
- [pstack-principle-laziness-protocol](../pstack-principle-laziness-protocol/SKILL.md)
- [pstack-principle-make-operations-idempotent](../pstack-principle-make-operations-idempotent/SKILL.md)
- [pstack-principle-migrate-callers-then-delete-legacy-apis](../pstack-principle-migrate-callers-then-delete-legacy-apis/SKILL.md)
- [pstack-principle-minimize-reader-load](../pstack-principle-minimize-reader-load/SKILL.md)
- [pstack-principle-model-the-domain](../pstack-principle-model-the-domain/SKILL.md)
- [pstack-principle-never-block-on-the-human](../pstack-principle-never-block-on-the-human/SKILL.md)
- [pstack-principle-outcome-oriented-execution](../pstack-principle-outcome-oriented-execution/SKILL.md)
- [pstack-principle-prove-it-works](../pstack-principle-prove-it-works/SKILL.md)
- [pstack-principle-redesign-from-first-principles](../pstack-principle-redesign-from-first-principles/SKILL.md)
- [pstack-principle-separate-before-serializing-shared-state](../pstack-principle-separate-before-serializing-shared-state/SKILL.md)
- [pstack-principle-sequence-verifiable-units](../pstack-principle-sequence-verifiable-units/SKILL.md)
- [pstack-principle-subtract-before-you-add](../pstack-principle-subtract-before-you-add/SKILL.md)
- [pstack-principle-test-behavior-not-implementation](../pstack-principle-test-behavior-not-implementation/SKILL.md)
- [pstack-principle-type-system-discipline](../pstack-principle-type-system-discipline/SKILL.md)

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-how](../pstack-how/SKILL.md)
- [pstack-architect](../pstack-architect/SKILL.md)
- [pstack-swarm](../pstack-swarm/SKILL.md)
- [pstack-interrogate](../pstack-interrogate/SKILL.md)
- [pstack-show-me-your-work](../pstack-show-me-your-work/SKILL.md)

## Source

Adapted from [pstack/skills/poteto-mode/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
