---
name: pstack-poteto-help
description: "Use when the user requests poteto help or its workflow. Identify the user's goal and recommend the smallest applicable skill or workflow from this catalog."
---

# Poteto Help

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

1. Identify the user's goal and recommend the smallest applicable skill or workflow from this catalog.
2. Explain actual host capabilities and setup state.
3. Do not invent slash commands, custom-mode UI, installation success or available models.
4. Distinguish the portable source proposal, installed personal skills, project-local procedures and optional runtime integrations.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-poteto-mode](../pstack-poteto-mode/SKILL.md)
- [pstack-setup-pstack](../pstack-setup-pstack/SKILL.md)

## Source

Adapted from [pstack/skills/poteto-help/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/poteto-help/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
