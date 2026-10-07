# autopilot stack

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Confirm that the requested deliverable is a reviewable stack and that landing remains with the operator. A request to state a plan does not authorize execution.
2. Give each unit an isolated lifecycle owner for implementation, proof, review findings and readiness. Use the verification-round and liveness discipline of [autopilot-full](autopilot-full.md), but no owner merges, arms auto-merge or closes a PR.
3. Owners report exact head, current base and intended parent. One coordinator alone owns stack topology; parallel owners write only their own implementation branches.
4. Append only independently verified patches to one linear base-branch chain. The root targets trunk and each child targets its parent’s exact tip. Perform rebases, retargeting and publication only under the applicable authorization and safe branch-update checks.
5. After trunk or parent movement, reconcile bottom-up and record every changed base and head. Changed patches require new verification; even unchanged patches require current-head checks and mergeability checks. Never silently reuse stale verdicts.
6. Deliver root and tip links, dependency order and evidence for each link, plus exclusions and outstanding gates. Stop at delivery without landing the chain; honor holds across all owners.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/autopilot-stack.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/autopilot-stack.md). Adapted under the [MIT license](../LICENSE).
