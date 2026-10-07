# perf issue

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Capture a baseline on the affected real surface and inspect its bottleneck. Apply the [benchmark-checklist procedure](../skills/pstack-benchmark-checklist/SKILL.md) to baseline and candidate measurements.
2. Ground hypotheses in the architecture. Prefer eliminating unused work, avoiding repeated work, reducing or deferring work, moving work off the critical path, concurrency, then cheaper execution; stop when the requested target is met.
3. Test one evidence-justified change at a time. Resolve boundary-crossing design before implementation and preserve correctness gates.
4. Capture and compare before/after artifacts under matching conditions. State uncertainty and reject wrong-surface or inconclusive performance claims.
5. Report primary metric, units, baseline, final value, delta and artifact locations. Use [hillclimb](hillclimb.md) for a separately requested sustained optimization run; publish only within scope.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/perf-issue.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/perf-issue.md). Adapted under the [MIT license](../LICENSE).
