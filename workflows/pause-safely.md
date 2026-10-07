# pause safely

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Honor an explicit pause or stop promptly; do not infer a pause from a user asking continued work.
2. Finish or back out of the current atomic step where safe, start no new work and stop owned child activity. Identify external processes that remain active.
3. Preserve recoverable edits and evidence without adding unapproved commits, pushes or other external actions. Record whether the working tree or artifact is incomplete.
4. Leave a supported durable handoff with intent, verified progress, exact revisions, current state, key files, gotchas and the first authorized resume step. Do not manufacture a follow-up schedule.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/pause-safely.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/pause-safely.md). Adapted under the [MIT license](../LICENSE).
