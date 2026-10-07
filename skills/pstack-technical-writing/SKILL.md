---
name: pstack-technical-writing
description: "Use when the user requests technical writing or its workflow. Choose tutorial, how-to, explanation or reference based on audience and purpose."
---

# Technical Writing

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- source.read (as needed)
- artifacts.write (only when saving is requested)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The requested artifact or change, relevant source/revisions, acceptance criteria, constraints and authorized output destination.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Drafting does not authorize posting or publishing. Follow the user's voice and existing document conventions over generic style rules.
2. Choose tutorial, how-to, explanation or reference based on audience and purpose. Keep tutorials focused on guided learning, how-to guides on a practical task, explanations on reasons and tradeoffs, and references on accurate lookup. Avoid mixing these purposes without clear separation.
3. Organize around the reader's question; use concrete verbs, stable terminology, explicit conditions and unambiguous references. Write procedures as direct actions, generally one action per step, with warnings and prerequisites before the action they constrain. Place only/not next to what they modify, give pronouns clear referents, and preserve articles or linking words when needed for unambiguous parsing.
4. Separate evidence from inference. Preserve technical accuracy, links and important caveats. Use actual symbols, paths, flags, and commands rather than invented synonyms. Verify counts, trees, and generated claims against the stated revision and include a regeneration command when applicable. Keep review summaries short and link detailed evidence instead of pasting full worker logs.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-unslop](../pstack-unslop/SKILL.md)

## Source

Adapted from [pstack/skills/technical-writing/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/technical-writing/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
