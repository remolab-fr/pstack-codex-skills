# investigation

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Read and cite scoped evidence, tracing how the subsystem works and why relevant decisions were made.
2. Compare competing explanations or decision alternatives and their tradeoffs. Separate facts, inference and unresolved gaps; challenge an unsupported premise.
3. Return the requested explanation or recommendation and stop. No implementation or PR is implied; route a subsequently authorized change to the appropriate workflow.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/investigation.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/investigation.md). Adapted under the [MIT license](../LICENSE).
