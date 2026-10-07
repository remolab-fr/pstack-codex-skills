# Triage Issue Reports

Operational reference procedure. Loading this file does not create or enable an automation.

## Before starting

Read the [portable execution contract](../../../../core/contract.md). Resolve host operations through the [Codex adapter](../../../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Inputs

Verified source channel/thread, authorized sender and repository, configured tracker/control adapter, safe test environment, bounded budgets and granted actions.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure
1. Load complete external configuration or stop without writes. Freeze the verified source channel and root-thread coordinates, confirm the existing parent and obtain its permalink. Never replace these coordinates with a reply or operations timestamp.
2. Read the whole report and current replies, including relevant media, logs, environment, expected/observed behavior and existing work links. Disclose unreadable attachments and use existing evidence before asking for more.
3. Trace the likely path and relevant history enough to separate cause from symptom and identify existing fixes. Classify bug, performance, feature request, question/feedback or configured reroute; uncertainty is not a new-bug verdict.
4. Apply only configured evidence-supported routes. Do not cross-post or guess an owner. Owner pings require their separate configured authorization and strong matching evidence.
5. Search prior verdicts and tracker issues by source permalink, signature, area, trigger, symptom and relevant version/history. A confident duplicate may receive an authorized source/recurrence update without changing unrelated fields; a plausible match remains uncertain and creates no new issue.
6. Create only a clearly broken, still-live bug/performance issue with no plausible live duplicate, a valid source backlink, resolved tracker fields and an available authorized reversible compensation action. Preserve expected/observed behavior, environment, evidence and labeled hypotheses; do not present guessed cause as fact.
7. Immediately before each ordinary tracker write and verdict post, recheck the source parent. If it is missing or uncertain, stop without that write. The only exception is the already-authorized reversible compensation for this run’s own newly created issue described in step 9; this does not permit a new issue, a normal tracker update, or a fallback post. Prepare exactly one substantive thread-only verdict ending in exactly one configured marker; marker type and optional tracker link must be unambiguous.
8. Only the authorized coordinator posts, using the frozen nonempty thread coordinates. Read back the verdict to confirm it landed under that parent. Never retry at channel root, another channel or a replacement thread.
9. If this run created an issue but cannot deliver its verdict, including source-parent preflight failure or disappearance, perform only the configured, already-authorized reversible compensation on that exact issue and verify its result. If that compensation itself lacks authority or capability, stop and report the unresolved issue instead. Report unverified compensation in the run output; never assume permanent deletion is permitted.
10. Use a bounded follow-up window only when authorized, answer direct questions or concrete corrections within scope, emit no second marker and stop when asked. Workers return evidence only and receive no Slack credentials/write capability; apply technical isolation wherever required.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Source

Adapted from [pstack/automations/benny/skills/triage-issue-reports/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/automations/benny/skills/triage-issue-reports/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [repository LICENSE](../../../../LICENSE).
