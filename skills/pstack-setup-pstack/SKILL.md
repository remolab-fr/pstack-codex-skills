---
name: pstack-setup-pstack
description: "Use when the user requests setup pstack or its workflow. Inspect the host's documented capabilities and actually available model controls."
---

# Setup Pstack

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- source.read (as needed)
- artifacts.write (only when saving is requested)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The requested configuration or procedure, its intended scope and destination, existing user-owned material, and evidence of what the host can actually support.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Inspect the host's documented capabilities and actually available model controls. On reconfiguration, read existing supported settings first and preserve unrelated role choices. Validate actual host-supported model and effort combinations rather than deriving identifiers by rewriting name strings.
2. Treat reasoning effort separately from model identity. Map abstract roles such as explorer, implementer, reviewer and synthesizer to host defaults; inherit the parent model unless an override is explicitly permitted. Distinguish a panel list, which sets candidate seats, from a judge pool, from which one judge is selected, and a worker default. Inherit the parent when no explicit supported override is permitted; configuration data alone does not establish active host behavior.
3. Report unsupported roles or constraints without inventing model names. Prepare configuration as data. Show the proposed mapping and any unsupported or retired entry before an authorized persistent update.
4. Persist only through the host's supported configuration or skill-management route after the relevant authorization, and verify the effect before claiming setup complete.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-poteto-help](../pstack-poteto-help/SKILL.md)

## Source

Adapted from [pstack/skills/setup-pstack/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/setup-pstack/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
