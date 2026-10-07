# visual parity

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Freeze reference screenshots and a repeatable visual harness before migration, covering requested states, dimensions and data. Without a baseline, make no parity claim.
2. Keep the baseline and harness immutable during the comparison. Do not edit the reference or restructure the component merely to hide a mismatch; surface a disputed baseline for a decision.
3. Migrate shared primitives first where necessary, then one component or independent isolated slice at a time.
4. Use image diffs on matching surfaces, not visual impression alone. For pixel-exact parity, every nonzero delta fails until explained and fixed; use a different tolerance only when explicitly agreed.
5. Check interactions as well as screenshots and repeat until the agreed criterion or genuine gate is reached. Report per-component diff result, baseline location and remaining gaps.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/visual-parity.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/visual-parity.md). Adapted under the [MIT license](../LICENSE).
