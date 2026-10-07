# Skill and workflow catalog

Repository source only. Read the [contract](core/contract.md) and [adapter](adapters/codex/README.md) before use. No entry here grants permission or installs itself.

## Skills
- [pstack-architect](skills/pstack-architect/SKILL.md): Ground the requested change in existing behavior and constraints.
- [pstack-arena](skills/pstack-arena/SKILL.md): Define the artifact and a task-specific rubric with 3–6 checkable criteria.
- [pstack-automate-me](skills/pstack-automate-me/SKILL.md): Find any existing user-owned working-style skill before proposing a new one.
- [pstack-benchmark-checklist](skills/pstack-benchmark-checklist/SKILL.md): Define the claim and baseline before measuring.
- [pstack-blast-radius](skills/pstack-blast-radius/SKILL.md): Read the diff and identify the invariant on which its safety depends.
- [pstack-bro](skills/pstack-bro/SKILL.md): Restate the last user-facing message in plain everyday language.
- [pstack-correct](skills/pstack-correct/SKILL.md): Identify a supported recurring mistake from the scoped task evidence.
- [pstack-create-verification-skill](skills/pstack-create-verification-skill/SKILL.md): Inspect the target repository for its real user surface, launch commands, existing control harness, observable evidence and isolation boundaries.
- [pstack-figure-it-out](skills/pstack-figure-it-out/SKILL.md): State the outcome, scope, constraints, available capabilities and done predicate.
- [pstack-how](skills/pstack-how/SKILL.md): For a narrow question, inspect the relevant source and explain it directly.
- [pstack-interrogate](skills/pstack-interrogate/SKILL.md): Fix the review scope and state intended behavior before review.
- [pstack-maintain-verification-skill](skills/pstack-maintain-verification-skill/SKILL.md): Locate the requested verification skill and read every feature-map entry.
- [pstack-make-bot-ui](skills/pstack-make-bot-ui/SKILL.md): Define a small UI action schema and a server-side dispatcher to an explicitly configured provider.
- [pstack-no-comments](skills/pstack-no-comments/SKILL.md): Review only the requested comments and their surrounding code.
- [pstack-poteto-help](skills/pstack-poteto-help/SKILL.md): Identify the user's goal and recommend the smallest applicable skill or workflow from this catalog.
- [pstack-poteto-mode](skills/pstack-poteto-mode/SKILL.md): Route the requested outcome to the narrowest workflow below.
- [pstack-principle-attack-the-premise](skills/pstack-principle-attack-the-premise/SKILL.md): After multiple fixes fail the same gate, identify their shared premise and test it directly.
- [pstack-principle-boundary-discipline](skills/pstack-principle-boundary-discipline/SKILL.md): Validate untrusted inputs at system boundaries and keep domain logic independent of framework adapters.
- [pstack-principle-build-the-lever](skills/pstack-principle-build-the-lever/SKILL.md): Prefer a small deterministic codemod, generator or verification tool when it makes substantial work reproducible.
- [pstack-principle-encode-lessons-in-structure](skills/pstack-principle-encode-lessons-in-structure/SKILL.md): For an evidenced recurring error, propose the strongest proportionate safeguard: ownership, types, lint, canonical helper, test or documentation.
- [pstack-principle-exhaust-the-design-space](skills/pstack-principle-exhaust-the-design-space/SKILL.md): When a consequential novel design lacks a clear precedent, compare a few genuinely different bounded alternatives against explicit criteria.
- [pstack-principle-experience-first](skills/pstack-principle-experience-first/SKILL.md): Evaluate product choices by the user's actual outcome and the quality of the complete interaction.
- [pstack-principle-explain-the-number](skills/pstack-principle-explain-the-number/SKILL.md): Before relying on a measured result, identify its limiting resource, validate that the intended work occurred, and check repeatability, output correctness and end-to-end significance.
- [pstack-principle-fix-root-causes](skills/pstack-principle-fix-root-causes/SKILL.md): Reproduce the failure and trace the causal path.
- [pstack-principle-foundational-thinking](skills/pstack-principle-foundational-thinking/SKILL.md): Before adding logic, choose structures and ownership that make valid behavior clear.
- [pstack-principle-guard-the-context-window](skills/pstack-principle-guard-the-context-window/SKILL.md): Keep the active context focused on relevant evidence and concise findings.
- [pstack-principle-laziness-protocol](skills/pstack-principle-laziness-protocol/SKILL.md): Prefer the smallest change that actually solves the problem.
- [pstack-principle-make-operations-idempotent](skills/pstack-principle-make-operations-idempotent/SKILL.md): Design retries and lifecycle transitions to converge safely after partial failure.
- [pstack-principle-migrate-callers-then-delete-legacy-apis](skills/pstack-principle-migrate-callers-then-delete-legacy-apis/SKILL.md): For an authorized internal API migration, enumerate real consumers, migrate them in verifiable units, and retire the obsolete API only after compatibility and rollback obligations are addressed.
- [pstack-principle-minimize-reader-load](skills/pstack-principle-minimize-reader-load/SKILL.md): Reduce unnecessary indirection and mutable scope so an engineer can answer a behavior question locally.
- [pstack-principle-model-the-domain](skills/pstack-principle-model-the-domain/SKILL.md): Represent meaningful states, ownership and transitions explicitly.
- [pstack-principle-never-block-on-the-human](skills/pstack-principle-never-block-on-the-human/SKILL.md): Proceed with useful work that is within the user's authorized scope and the host's permission rules.
- [pstack-principle-outcome-oriented-execution](skills/pstack-principle-outcome-oriented-execution/SKILL.md): Use explicit phase boundaries and verified outcomes to converge on the target design.
- [pstack-principle-prove-it-works](skills/pstack-principle-prove-it-works/SKILL.md): Verify the actual requested result through its real surface or artifact before claiming success.
- [pstack-principle-redesign-from-first-principles](skills/pstack-principle-redesign-from-first-principles/SKILL.md): When a new requirement exposes a flawed structure, compare a coherent redesign against a minimal extension.
- [pstack-principle-separate-before-serializing-shared-state](skills/pstack-principle-separate-before-serializing-shared-state/SKILL.md): Give parallel workers separate writable outputs and clear ownership.
- [pstack-principle-sequence-verifiable-units](skills/pstack-principle-sequence-verifiable-units/SKILL.md): Break a multi-step effort into units with observable acceptance checks and explicit dependencies.
- [pstack-principle-subtract-before-you-add](skills/pstack-principle-subtract-before-you-add/SKILL.md): Remove proven dead or redundant structure when it simplifies the authorized change.
- [pstack-principle-test-behavior-not-implementation](skills/pstack-principle-test-behavior-not-implementation/SKILL.md): Exercise the interface used by real callers and assert meaningful expected results.
- [pstack-principle-type-system-discipline](skills/pstack-principle-type-system-discipline/SKILL.md): Model invalid states out of existence where practical.
- [pstack-recall](skills/pstack-recall/SKILL.md): Use a supplied current-state capsule when sufficient.
- [pstack-reflect](skills/pstack-reflect/SKILL.md): Review only the active task's available evidence or a user-authorized transcript export.
- [pstack-setup-pstack](skills/pstack-setup-pstack/SKILL.md): Inspect the host's documented capabilities and actually available model controls.
- [pstack-show-me-your-work](skills/pstack-show-me-your-work/SKILL.md): Maintain a concise outcome/evidence record for a long or unattended task: timestamp, phase, decision summary, public rationale, evidence reference and result.
- [pstack-swarm](skills/pstack-swarm/SKILL.md): Define the done predicate and choose partitioned coverage, independent races or a mixed shape.
- [pstack-tdd](skills/pstack-tdd/SKILL.md): Use when explicitly requested or when a practical local regression test is clear.
- [pstack-teach](skills/pstack-teach/SKILL.md): Choose what the user needs to understand from the question and visible context.
- [pstack-technical-writing](skills/pstack-technical-writing/SKILL.md): Choose tutorial, how-to, explanation or reference based on audience and purpose.
- [pstack-typescript-best-practices](skills/pstack-typescript-best-practices/SKILL.md): Follow the repository's TypeScript configuration and conventions.
- [pstack-unslop](skills/pstack-unslop/SKILL.md): Rewrite the requested prose to remove filler, unsupported claims, decorative structure and vague abstractions while preserving meaning, uncertainty, required terminology and audience.
- [pstack-why](skills/pstack-why/SKILL.md): Anchor the question in exact code, commits, PRs or observed behavior.

## Workflows
- [investigation](workflows/investigation.md)
- [bug-fix](workflows/bug-fix.md)
- [perf-issue](workflows/perf-issue.md)
- [hillclimb](workflows/hillclimb.md)
- [runtime-forensics](workflows/runtime-forensics.md)
- [trace-forensics](workflows/trace-forensics.md)
- [feature](workflows/feature.md)
- [refactoring](workflows/refactoring.md)
- [prototype](workflows/prototype.md)
- [visual-parity](workflows/visual-parity.md)
- [authoring-a-skill](workflows/authoring-a-skill.md)
- [eval](workflows/eval.md)
- [babysit](workflows/babysit.md)
- [shipping](workflows/shipping.md)
- [autonomous-run](workflows/autonomous-run.md)
- [orchestrate](workflows/orchestrate.md)
- [autopilot-full](workflows/autopilot-full.md)
- [autopilot-stack](workflows/autopilot-stack.md)
- [session-pickup](workflows/session-pickup.md)
- [pause-safely](workflows/pause-safely.md)
- [multi-phase-plan](workflows/multi-phase-plan.md)
- [worktree-cleanup](workflows/worktree-cleanup.md)
- [opening-a-pr](workflows/opening-a-pr.md)

## Inactive operational procedures
- [pstack-reproduce-and-fix-issues](integrations/benny/procedures/reproduce-and-fix-issues/PROCEDURE.md)
- [pstack-setup-benny](integrations/benny/procedures/setup-benny/PROCEDURE.md)
- [pstack-triage-issue-reports](integrations/benny/procedures/triage-issue-reports/PROCEDURE.md)
