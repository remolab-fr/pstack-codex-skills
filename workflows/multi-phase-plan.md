# multi phase plan

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Treat the plan as the deliverable, not permission to implement. If the task is too small to benefit from a multi-phase plan, explain that rather than inventing ceremony.
2. Resolve empirical unknowns with authorized, isolated prototypes where useful. Record evidence and unanswered product decisions before fixing dependencies.
3. Define one independently verifiable change per phase or PR: dependency, owner, allowed files, build steps, observable outcome and delivery artifact.
4. For each unit, specify concrete unit, real-surface and relevant performance checks with pass/fail criteria. Compare like-for-like baseline and candidate workloads; if the baseline lacks a feature, specify absolute budgets for added work rather than a misleading ratio.
5. Name the execution workflow, topology owner, evidence freshness rule and who may land changes. Explicitly identify interaction-review or other operator gates and the evidence needed to resolve them.
6. Validate dependency order, file ownership, reachable references, completeness of placeholders and verification commands using host-supported checks. Do not run omitted upstream validators implicitly.
7. Include prototype evidence, rejected alternatives, risks and relevant references. Deliver the plan and validation result, then wait for execution authorization.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/multi-phase-plan.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/multi-phase-plan.md). Adapted under the [MIT license](../LICENSE).
