# autonomous run

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Record the bounded goal, checkable outcome predicate, permitted changes, budget and recovery policy before the first iteration. Do not weaken the predicate to declare success.
2. Use supported event notifications or a host-supported wait mechanism, with a suitable fallback check when needed. Do not fabricate a watcher or create recurring work without authorization.
3. Make one evidence-justified change, verify it against the predicate, and retain only improvements. Revert your ineffective experimental changes safely; preserve unrelated user work.
4. Checkpoint every iteration with the change, observable result and predicate state. Verify each unit before starting the next.
5. Continue through temporary failures and plateaus; change approach when evidence warrants. Fix only discoveries within scope, and surface out-of-scope work without silently expanding the task.
6. Pause dependent work at genuine authorization/capability gates while continuing independent authorized work. Stop at the agreed outcome, budget or stopping condition, cancellation, lost relevance or a documented dead end.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/autonomous-run.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/autonomous-run.md). Adapted under the [MIT license](../LICENSE).
