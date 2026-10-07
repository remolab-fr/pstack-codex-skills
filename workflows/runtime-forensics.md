# runtime forensics

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Capture the authorized live signal with appropriate safe instrumentation: for example a CPU profile, heap snapshot or interaction trace. Source speculation is not a runtime finding.
2. Reduce the artifact to the relevant hot path, retention chain or repeated activity. Delegate bulk parsing if useful and retain source-linked evidence.
3. Test the suspected mechanism with authorized, non-destructive observations or instrumentation. Runtime mutation or hot patching requires its own scope; if unavailable, label the causal conclusion as unconfirmed.
4. Map the finding to source file and symbol, distinguish observations from inference, and return capture conditions and artifacts. Diagnosis is the deliverable; repairs require separate scope.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/runtime-forensics.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/runtime-forensics.md). Adapted under the [MIT license](../LICENSE).
