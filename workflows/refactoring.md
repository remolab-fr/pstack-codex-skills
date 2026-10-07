# refactoring

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Pin existing behavior before structural changes using a characterization test, snapshot or equivalence harness. Compilation and lint alone do not establish the behavior contract.
2. Name the missing structure and target module/type/call-graph shape; avoid indirection without a concrete reader-load benefit. Resolve cross-boundary design before moving code.
3. Move in small behavior-preserving steps, keeping the pin green. Remove justified dead structure, migrate actual consumers and check strings, documentation and back-references as well as typed callers.
4. Preserve compatibility contracts until consumers and authorized migration scope are established. Separate newly discovered features or behavior fixes from the structural change.
5. Prove equivalence on the real artifact or a representative replay. Assess whether the result reduces reader load; revert your speculative changes safely if they provide no benefit.
6. Return structural change, contract pin, equivalence evidence and remaining compatibility gaps. Commit or publish only within authorized scope.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/refactoring.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/refactoring.md). Adapted under the [MIT license](../LICENSE).
