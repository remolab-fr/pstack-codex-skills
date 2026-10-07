# babysit

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Choose status-only, review-only, background or drive-to-ready from the request. Status-only performs one pass. Verify the repository, active forge, exact heads and frozen bottom-up queue before polling.
2. Use one babysitter per stack and prioritize its lowest unmerged frontier. Read and batch upper-stack findings without restarting frontier checks unnecessarily.
3. Keep topology with the designated owner: report conflicts and required base reconciliation rather than independently retargeting, rebasing or force-pushing. A fix to already-merged code needs a separately authorized follow-up change, not rewritten history.
4. Handle conflicts, supported review findings and CI in that order. Verify review claims against code; batch real fixes into a coherent push wave on the branch that owns the code, with regression evidence. Reply only under communication scope.
5. Classify CI failures before retrying. Distinguish changed-code defects, stale-base failures and infrastructure/flake evidence. Allow one justified fresh run for a suspected transient failure; an identical repeat needs diagnosis rather than blind retries.
6. Read current forge mergeability, required checks, approvals and unresolved blockers together. A green check list alone is not merge-ready. Recheck exact-head status after each change and use only supported observation tools.
7. Continue drive mode until the requested readiness condition or a genuine blocker; answer user questions without silently abandoning the watch. Ready, pending, failed, merged, canceled and unknown remain distinct.
8. Stop at readiness and report frontier, fixes, dismissed findings with evidence and remaining human gates. Babysitting never itself authorizes merge or auto-merge; route authorized landing to [shipping](shipping.md).

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/babysit.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/babysit.md). Adapted under the [MIT license](../LICENSE).
