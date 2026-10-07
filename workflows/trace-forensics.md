# trace forensics

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Inspect the supplied capture as a fixed artifact; identify format, capture conditions and limitations rather than silently recapturing it.
2. Use suitable parsers to make large traces or heap data queryable, then narrow to hot frames, retention paths, blocked threads or wait reasons.
3. Map findings to source through the artifact’s symbols. Missing symbol resolution is an explicit limitation, not a fabricated source diagnosis.
4. Compare a paired before/after capture when available. Without discriminating corroboration, label the result as the strongest supported hypothesis rather than confirmed cause.
5. Return cited findings, source locations and artifact references. Do not implement a fix unless separately authorized.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/trace-forensics.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/trace-forensics.md). Adapted under the [MIT license](../LICENSE).
