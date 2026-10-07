# shipping

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Require explicit authority to land the named change or stack. Freeze bottom-up order and obtain independent verification of each patch on the relevant real surface against its parent or appropriate baseline. The verifier must not be its implementer; CI or bot approval alone is not a behavioral verdict.
2. Record each verdict’s head, base and patch identity. Stop the landable run at the first unverified PR; verification above a gap does not make it landable.
3. Before landing, compare current patch and evidence with the verified revision. Changed patches invalidate prior verdicts; reverify affected evidence. Unchanged patches still require current-head checks and mergeability. Do not substitute old green checks or matching commit messages.
4. Prepare only the current bottom PR, with authorized rebase/retarget operations and re-verification afterward. Do not arm, retarget or merge descendants prematurely.
5. Land one PR at a time. Auto-merge requires applicable authorization and confirmation from the active forge; a queued or ready state is not proof of merger.
6. Watch the frontier until it actually merges or reaches a genuine failure/blocker. Pending requirements are not failure. Diagnose a stall before changing topology.
7. After merger, confirm the landed commit on trunk, recompute the remaining frontier, inspect the next PR’s current base/head/checks and repeat. Do not assume automatic retargeting worked.
8. Stop at the verified ceiling and report landed commits, remaining PRs and the evidence needed to extend the run.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/shipping.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/shipping.md). Adapted under the [MIT license](../LICENSE).
