---
name: pstack-figure-it-out
description: "Use when the user requests figure it out or its workflow. State the outcome, scope, constraints, available capabilities and done predicate."
---

# Figure It Out

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

1. State the outcome, scope, constraints, available capabilities and done predicate. When no narrower workflow fits, design a sequence of verifiable units with explicit hypotheses and evidence gates. Before an ambitious run, quantify the units of work and known blockers, choose rigor proportional to consequence, and present the designed phase list. Capture a pre-change baseline and build the verification method before changing the artifact.
2. Keep user-visible decision summaries rather than private reasoning.
3. Order units by risky unknowns and dependencies. Give each experiment a hypothesis, minimal change, real-artifact measurement, and keep/revert decision. Do not count INCONCLUSIVE as verified. Choose experiments that distinguish hypotheses, record results and revise the plan from evidence.
4. Continue authorized independent work while a gate is blocked. Judge delegated artifacts directly. If a worker exploits a weak check, strengthen the contract; if the check is wrong, repair it as an explicit separate change. Record decisions as each unit lands, then verify the complete product against the original done predicate.
5. Return the result, evidence, unresolved decisions and a concrete next step.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-show-me-your-work](../pstack-show-me-your-work/SKILL.md)
- [pstack-architect](../pstack-architect/SKILL.md)

## Source

Adapted from [pstack/skills/figure-it-out/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/figure-it-out/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
