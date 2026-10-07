# orchestrate

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Confirm a standing multi-unit program is warranted; use a simpler workflow for work one owner can finish. Define countable completion, dependencies, budget, tracks and authorized landing scope.
2. Maintain supported durable records for unit owner, branch, PR, exact head, state, evidence, pending gates and decisions. Derive status from those records; one writer owns each shared resource.
3. Each worker brief carries goal, allowed and forbidden paths/actions, relevant upstream findings, acceptance criteria, verification method, timebox and return format. Relay current user constraints on every handoff without broadening authority.
4. Pilot one representative unit through implementation, verification and authorized delivery before scaling. Use the pilot to correct the brief and verification recipe.
5. Use a rolling window within available capacity. Recompute ready work as results arrive, relay dependency evidence and reconcile every completion without disrupting atomic shared-state operations.
6. Keep one topology owner per stack and a computed bottom-up frontier. Workers report conflicts; they do not independently rewrite shared topology. Integrate verified units progressively only if landing is authorized.
7. Key verification to PR, head and base/patch identity. Distinguish live verification, unit-only evidence, typecheck-only, blocked and failed. CI green and blocked verification are not proof of behavior; changed patches invalidate prior evidence.
8. Inspect durable progress for liveness, classify failures and retry within a bounded recovery policy. Reconcile late results against current revisions before accepting them; do not merge stale work blindly.
9. After interruption, reconstruct from durable records and current external state. At close, reconcile all children, externalize authorized deliverables, verify the completion predicate and report abandoned units and unresolved gates.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/orchestrate.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/orchestrate.md). Adapted under the [MIT license](../LICENSE).
