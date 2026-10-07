# Reproduction run template

Status: disabled example, not a standing instruction or grant of permission.

Before launching the app, executing reproduction code or driving the live surface, verify the execution boundary excludes Slack credentials and write tools as required by the Benny threat model. A prompt-only write ban is insufficient. If equivalent isolation cannot be demonstrated, block execution and return findings only; do not substitute an equally privileged coordinator.

Use the [reproduction procedure](../procedures/reproduce-and-fix-issues/PROCEDURE.md) only with a verified trusted triage marker on an existing in-scope thread. After the isolation preflight succeeds, reproduce the exact symptom twice in a disposable safe environment. Check for an existing fix before proposing new code. Preserve before/after evidence.

Fixes, draft PRs and status posts require the actual configured permission and budget. Stop at the approved condition and report incomplete evidence honestly.
