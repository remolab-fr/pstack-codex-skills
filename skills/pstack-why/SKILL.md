---
name: pstack-why
description: "Use when the user requests why or its workflow. Anchor the question in exact code, commits, PRs or observed behavior."
---

# Why

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

The question or topic, known source anchors, relevant time window and available authorized evidence sources.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Git, command-line tools and external accounts are not assumed available. Anchor the question in exact code, commits, PRs or observed behavior. Trace historical anchors through renames and earlier substantive changes, not just the latest commit. Bring paths, symbols, commits, PR discussion, and linked issues to each relevant read-only investigator. Defensive code warrants a search for incidents and earlier failed fixes.
2. Discover available evidence sources by capability: source history, issues, documents, team discussions, infrastructure telemetry, error tracking and product analytics. Search only relevant authorized sources and report unavailable or skipped categories. Record a coverage map for source history, issues, documents, team discussion, infrastructure telemetry, errors, and product analytics. For each relevant category state what was searched and found, including null results, unavailable tools, or an explicit scope-based reason to skip. A source returning nothing is not proof that the motivating concern never existed.
3. Investigators separate chronology, correlation and actual evidence of motivation. Classify claims as direct author statement, supported by converging evidence, inferred, speculative, or unknown. Code proves behavior, not author intent. Treat a hypothesis embedded in the user’s question as one candidate to test, and preserve conflicting accounts with citations.
4. Synthesize competing explanations, confidence and source citations; for a proposed change, extract Preserve, Change, Avoid and Risk constraints. Before delivery, check citations and confidence language claim by claim. Separate findings, inference, competing hypotheses, and unknowns. Preserve these distinctions when summarizing; do not retrofit a tidy rationale onto incomplete history. For contemplated edits derive Preserve, Change, Avoid, and Risk constraints from the verified lineage.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-how](../pstack-how/SKILL.md)

## Source

Adapted from [pstack/skills/why/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/why/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
