---
name: pstack-interrogate
description: "Use when the user requests interrogate or its workflow. Fix the review scope and state intended behavior before review."
---

# Interrogate

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- source.read
- source.compare (when relevant)
- delegation (optional)
- execution.run (proof only when authorized)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The requested artifact or change, relevant source/revisions, acceptance criteria, constraints and authorized output destination.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Review does not authorize publishing comments, changing code or merging. Fix the review scope and state intended behavior before review.
2. Use the complete requested changeset and necessary callers, callees, and types. Apply relevant lenses: intended behavior and edge cases; error propagation; retries and partial failure; structural concurrency control; root cause; ownership and representation leakage; realistic verification; complexity; and security. Give independent reviewers the same source/diff, constraints and rubric without suggesting the desired verdict.
3. For suspected correctness or security defects, trace the concrete input or call path to the failure, not merely a possible null or dangerous sink. Check real artifacts and integration paths rather than accepting worker self-reports or mock-only tests. Collect severity, mechanism, evidence and proposed test for each finding.
4. Deduplicate, preserve disagreements and assess lone-reviewer findings on evidence rather than vote count. The lead decides what to act on, consider, dismiss or leave unresolved. Retain per-reviewer attribution and categorize each finding as act on, consider, noted, or dismissed with a short reason. State actual reviewer/model diversity, gaps, and contradictions. The lead’s evidence-based judgment is the deliverable, not an automatic patch.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-blast-radius](../pstack-blast-radius/SKILL.md)
- [pstack-no-comments](../pstack-no-comments/SKILL.md)

## Source

Adapted from [pstack/skills/interrogate/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/interrogate/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
