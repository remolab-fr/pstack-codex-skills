# worktree cleanup

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Audit only the authorized repository and worktrees through supported metadata. Enumerate actual worktree paths and record disk usage, branch/merge status, tracked and untracked changes and active usage.
2. Treat classifications as candidates, not permission. Cross-check active or reserved work and related worker worktrees through supported task state; never inspect protected transcripts.
3. Treat untracked files as potentially valuable, closed/unmerged PRs as unverified and unknown usage as a reason to preserve. Document preservation evidence for each proposed removal.
4. Delete only the approved confirmed set, protecting the main worktree, user edits, active work and unverified content. Do not broaden a worktree request into simulator or cache deletion without scope.
5. Re-list worktrees and remeasure disk usage afterward. Report confirmed reclaimed space, removed paths and each held-back candidate’s reason.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/worktree-cleanup.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/worktree-cleanup.md). Adapted under the [MIT license](../LICENSE).
