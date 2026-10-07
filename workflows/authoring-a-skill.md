# authoring a skill

Read the [portable execution contract](../core/contract.md) and use the active [host adapter](../adapters/codex/README.md). This is a workflow, not a grant of authority.

## Start
Record the requested outcome, exact targets and revisions, available capabilities, permitted changes, evidence requirements and stopping condition. Confirm that this workflow fits; choose a narrower procedure when it does.

## Workflow
1. Use the host’s canonical skill-authoring workflow and preserve intended triggers, permissions, references and destination.
2. Validate required frontmatter, referenced files and cross-skill links. Exercise structural changes with representative cases; distinguish subjective editorial review from executable validation.
3. Keep instructions decision-relevant and link structural sources rather than restating them. Return design decisions and validation evidence.
4. Run the [opening-a-pr workflow](opening-a-pr.md) only within authorized delivery scope. A proposal is not installed; verify canonical persistence before claiming installation.

## Gate handling
If a required capability or approval is missing, pause the dependent step, state the exact blocker and continue useful independent authorized work. A denied action stays denied across tools. Do not run an upstream helper or install a dependency to bypass the gate.

## Result
Report complete, partial, blocked, failed or canceled. Link verified artifacts, state exactly what was checked, and preserve recoverable work and evidence. Publication, merge, scheduling and installation status must be explicit.

Source: [pstack/skills/poteto-mode/playbooks/authoring-a-skill.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-mode/playbooks/authoring-a-skill.md). Adapted under the [MIT license](../LICENSE).
