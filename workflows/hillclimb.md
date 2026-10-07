# hillclimb

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Ground the architecture and realistic workload before choosing a metric. Reproduce the complaint, then agree the metric, improvement direction, target, iteration floor if appropriate, budget and stop condition.
2. Build a repeatable measurement harness and prove its sensitivity with contrasting realistic workloads. Apply the [benchmark-checklist procedure](../skills/pstack-benchmark-checklist/SKILL.md), then freeze the harness, workload and acceptance gates; measure baseline noise and a green correctness baseline.
3. Keep a per-attempt log of hypothesis, change, before/after values, work/error counts, regression results and kept/reverted verdict. Read prior attempts before choosing the next hypothesis.
4. Test one architecture-grounded hypothesis at a time. Independent experiments may run in isolated worktrees, but never stack unmeasured changes.
5. Compare repeated measurements against the frozen baseline and run regression gates. Retain a change only when the gain exceeds noise and correctness holds; otherwise revert your experiment safely. Record simplifications that preserve performance separately from speed claims.
6. On a plateau, reconsider the mechanism or experiment category before declaring a dead end. Never relax the target to claim success or keep a faster result that breaks behavior.
7. Stop at the agreed predicate, budget, cancellation or genuine gate. Report baseline-to-final delta, accepted and rejected attempts, evidence and the next plausible experiment. Commit or publish only when authorized.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/hillclimb.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/hillclimb.md). Adapted under the [MIT license](../LICENSE).
