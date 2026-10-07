# feature

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Clarify observable behavior and acceptance criteria; inspect the affected subsystem and existing ownership before choosing a design.
2. Explore plausible designs and choose data structures, interfaces and state representation before implementation. Use independent alternatives or review when design choices materially affect the result.
3. Record blocking prerequisites, independent workstreams, shared mutable state and the smallest safe decomposition. Run gates before fan-out and keep coupled code under a coherent owner.
4. Implement scoped, independently verifiable units. Give workers exact paths, chosen domain shape and success criteria; serialize shared writes and migrate all consumers of changed shared primitives.
5. Verify the real user path and relevant consumers. Inconclusive or wrong-surface evidence is not success. Resolve contested design questions before authorized delivery.
6. Return what was built, decisions and evidence, remaining gaps and delivery state. Open a PR only within the requested delivery scope.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/feature.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/feature.md). Adapted under the [MIT license](../LICENSE).
