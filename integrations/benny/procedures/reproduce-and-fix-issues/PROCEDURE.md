# Reproduce And Fix Issues

Operational reference procedure. Loading this file does not create or enable an automation.

## Before starting

Read the [portable execution contract](../../../../core/contract.md). Resolve host operations through the [Codex adapter](../../../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Inputs

The requested artifact or change, relevant source/revisions, acceptance criteria, constraints and authorized output destination.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Isolation preflight

Before code execution, app launch, live-surface reproduction or a fix, verify the execution boundary excludes Slack credentials and Slack write tools where the Benny threat model requires isolation. A read-only prompt is insufficient. If the boundary cannot be demonstrated, block the execution-dependent work and return findings only. Do not substitute an equally privileged coordinator.

## Procedure
1. Require complete configuration, a safe test environment, a control adapter and a completed feature map. Freeze the source channel/root-thread coordinates and permalink; confirm the parent. Before any execution, satisfy the isolation preflight above.
2. Wait only within the configured authorized verdict budget. Accept exactly one configured bug/performance marker from the trusted triage identity in this exact thread. Stop for other, absent, conflicting or untrusted markers and timeouts.
3. Re-read ownership immediately before work. If a person claims the fix or explicitly assigns implementation, stop new implementation rather than race them. A diagnosis request or bot hypothesis alone is not fix ownership. A plausible existing PR/commit permits verification-only work under the existing authorized scope only when that does not conflict with the person’s instruction; their message is not a new grant of authority. Do not edit the artifact or create a competing patch.
4. Load the relevant feature-map path and verify the adapter can identify and launch the correct app/revision, drive real UI actions, reset state, inspect without mutation, capture screenshots/recordings and clean up. Missing capabilities are blocked, not a substitute unit-test reproduction.
5. Study the report, environment, media, history and competing causal hypotheses. Confirm the correct account, workspace, fixtures and app markers. State the expected and broken final states, then reach their discriminating point through real user interaction twice with an independent reset. Never inject internal state to force the symptom.
6. Capture the complete path and broken final state. Have an independent read-only reviewer verify that the media shows the discriminating defect. If evidence is absent or uncertain, return could-not-reproduce or blocked within budget; do not author a fix.
7. Keep detailed status/evidence in an authorized operations thread or run output. A confirmed reproduction may receive at most one authorized unsolicited source-thread update, with fresh parent preflight and read-back. Never post source-channel roots or use fallback destinations. Respect configured retention before attaching evidence.
8. When configured and authorized, allow the bounded rejection window for correction of the reproduction. Recheck human ownership and existing fix artifacts before beginning a fix; a valid correction, claimed ownership or new artifact stops ordinary fix work.
9. For an existing fix, record baseline and patched revisions and identical environment inputs. Reproduce twice on baseline and verify expected behavior twice on the running patched build. Distinguish confirmed, insufficient and inconclusive outcomes. No baseline reproduction means no claim that the fix works, and no competing PR follows an insufficient result.
10. Qualify a new fix only after confirmed media-backed reproduction, runtime-supported root cause, no conflicting ownership/artifact, a bounded authorized change and the ability to run baseline and patched builds. Use a cheap failing regression test where feasible; state unavailable test paths and keep unrelated cleanup out.
11. Preserve baseline evidence. On the patched build repeat the same real user path twice, capture expected final state and the same read-only cross-check, run focused required checks and smoke relevant neighboring states/failure paths. Stop without a PR when proof or regression gates fail.
12. Review the final diff for scope and secrets. Create a draft PR only when authorized and all proof gates pass; include root cause, before/after evidence, tests and blast-radius checks. Never merge or deploy from this procedure. Verify the URL/state and distinguish creation failure from success.
13. Use only configured authorized follow-ups. Always stop owned test processes and disposable sessions, clean temporary state safely and retain artifacts only for the permitted period. Keep Slack credentials/write tools outside execution workers and never substitute an equally privileged coordinator for missing isolation.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Source

Adapted from [pstack/automations/benny/skills/reproduce-and-fix-issues/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/automations/benny/skills/reproduce-and-fix-issues/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [repository LICENSE](../../../../LICENSE).
