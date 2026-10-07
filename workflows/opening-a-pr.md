# opening a pr

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Confirm PR creation lies within the requested delivery scope. Verify repository, destination base, branch and diff; isolate unrelated work and preserve it.
2. Shape changes into reviewable units and ordered commits when authorized. For a stack, root targets trunk and each child targets its actual parent; independent changes remain independent.
3. Run repository-required checks and inspect the final diff for unintended changes, unsafe comments and secrets. Record actual evidence and known gaps.
4. Prepare a concise description of the problem, change, scope, tradeoffs, blast radius and verification. Follow the user’s and repository’s writing conventions rather than forcing an upstream author’s style.
5. Use the host’s supported PR operation, honoring any required native tool and requested draft/readiness state. Verify the created URL, base, head and state before reporting success.
6. Opening a PR does not itself authorize babysitting, merging or auto-merge. Continue only the lifecycle work included in the user’s scope.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/opening-a-pr.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/opening-a-pr.md). Adapted under the [MIT license](../LICENSE).
