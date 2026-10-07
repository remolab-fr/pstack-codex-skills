---
name: pstack-automate-me
description: "Use when the user requests automate me or its workflow. Find any existing user-owned working-style skill before proposing a new one."
---

# Automate Me

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- history.search or supplied task evidence
- source.read
- artifacts.write (approved persistent changes only)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The requested configuration or procedure, its intended scope and destination, existing user-owned material, and evidence of what the host can actually support.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Find any existing user-owned working-style skill before proposing a new one. For an update, preserve the existing skill identity and unaffected sections, and concentrate on new evidence since its last revision. Do not replace a mode merely because a new draft is easier.
2. Use only authorized conversation context and explicit preferences or repeated evidence. Separate preferences from permission rules; a style skill cannot create standing authorization. Do not mine private transcript directories or automatically commit, publish or install the result.
3. Cluster observed conventions by response style, delegation, verification, code/prose discipline, and process. Ask a small number of focused questions about gaps that context cannot establish. Do not promote conflicting one-off choices into durable preferences.
4. Keep only concrete non-default conventions; reference other skills rather than duplicating them. Use narrow personal-mode triggers rather than generic coding keywords, then iterate on the draft with the user. Persistent permission changes belong to the host permission mechanism. Draft a concise set of working conventions and show the user the proposed change.
5. Use the host's skill-authoring workflow only after approval for the actual persistent change.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-reflect](../pstack-reflect/SKILL.md)
- [pstack-unslop](../pstack-unslop/SKILL.md)

## Source

Adapted from [pstack/skills/automate-me/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/automate-me/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
