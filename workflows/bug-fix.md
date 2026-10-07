# bug fix

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Reproduce the reported symptom on the matching real user surface. If that surface is unavailable, name the specific blocker; do not call a wrong-surface or inconclusive result a pass.
2. Form competing hypotheses from the affected subsystem and regression history. Choose discriminating experiments and runtime evidence until the causal mechanism is supported. Revert changes whose hypothesis is disproved.
3. Choose the smallest justified fix. For boundary-crossing changes, resolve the design before implementation and give any implementer a precise scope.
4. Where a cheap local regression path exists, demonstrate its failure before the fix and its success afterward; use ordered commits only if committing is authorized. State why a costly or unavailable test was skipped.
5. Rerun the original surface and relevant surrounding behavior after the fix. Return root cause, exact before/after evidence, remaining uncertainty and authorized delivery status.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/bug-fix.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/bug-fix.md). Adapted under the [MIT license](../LICENSE).
