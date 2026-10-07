# autopilot full

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Freeze the authorized queue, per-PR permissions, operator-reserved items and stop conditions. A request to state a plan is not permission to execute it.
2. Give each independent PR one lifecycle owner and its own branch or worktree. Parallelize disjoint work; serialize genuine overlap. Keep independent PRs independent rather than stacking them.
3. Each owner creates a durable evidence trail, implements in verifiable units, runs repository-required checks, reviews the diff and supported review findings, and reports the exact code-ready head. Publish branches and PRs only within granted scope.
4. For each code-ready patch, run independent verification: required gates, the actual user surface, a comparison with trunk where meaningful, and focused diff/risk review. Where trunk lacks the feature, test the added behavior and the intended user-visible end state instead of inventing a baseline result.
5. Consolidate proven findings into a fix round. Require a regression test or reproducible evidence for behavior defects, and carry those defects into the next review brief. A changed patch invalidates earlier verdicts; bind every verdict to head, base and patch identity.
6. Before an authorized merge, verify the current head’s checks, mergeability and applicability of all evidence. Rebase or reconcile conflicting or relevant overlapping trunk changes through the branch owner, then reverify affected evidence. Never force-push a shared branch.
7. The lifecycle owner may merge only after the coordinator’s clean verdict and actual merge authorization. Operator-reserved PRs stop at merge-ready. Refill the queue with fresh scoped owners as work completes.
8. Use a supported liveness audit during the run. Track children, expected progress and durable outputs; diagnose stalled workers and replace them when appropriate without losing their scope. Reconcile every child before closing the program.
9. On hold or stop, promptly stop new writes across owners and preserve recoverable state. Report each PR’s owner, head, evidence, status, completed merges and remaining gates.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/autopilot-full.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/autopilot-full.md). Adapted under the [MIT license](../LICENSE).
