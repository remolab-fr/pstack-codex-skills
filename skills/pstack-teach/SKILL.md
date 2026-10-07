---
name: pstack-teach
description: "Use when the user requests teach or its workflow. Choose what the user needs to understand from the question and visible context."
---

# Teach

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

1. This is an explanation task, not authority to change the system. Choose what the user needs to understand from the question and visible context.
2. Combine scoped [pstack-how](../pstack-how/SKILL.md) and [pstack-why](../pstack-why/SKILL.md) findings into a plain definition followed by a concrete mechanism, tradeoffs and relevant edge cases. Preserve the confidence of historical why findings when simplifying their wording. Explain actual mechanisms and user-visible flow rather than substituting metaphors or lists of function names.
3. Begin with the smallest complete explanation and add depth at the user's pace. Use diagrams or examples when the host supports them and they clarify the subject. Build complex explanations in successive layers and, when helpful and supported, progressively add components to diagrams. Let the user’s follow-up set the pace; do not add unsolicited quizzes or require them to repeat the lesson.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-how](../pstack-how/SKILL.md)
- [pstack-why](../pstack-why/SKILL.md)

## Source

Adapted from [pstack/skills/teach/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/teach/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
