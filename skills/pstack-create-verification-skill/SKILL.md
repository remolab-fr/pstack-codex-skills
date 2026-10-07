---
name: pstack-create-verification-skill
description: "Use when the user requests create verification skill or its workflow. Inspect the target repository for its real user surface, launch commands, existing control harness, observable evidence and isolation boundaries."
---

# Create Verification Skill

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- source.read
- execution.run (when needed and authorized)
- artifacts.write (within scope)
- delegation (optional)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The requested configuration or procedure, its intended scope and destination, existing user-owned material, and evidence of what the host can actually support.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Inspect the target repository for its real user surface, launch commands, existing control harness, observable evidence and isolation boundaries. Do not silently repair unrelated application problems. Use the host-authorized skill destination and authoring workflow, not a hardcoded IDE directory.
2. The generated instructions must name the primary user surface, exact launch command, readiness signal, required environment/authentication/seed state, and whether concurrent instances are safe. Prefer existing harnesses and stable labels or selectors over coordinates. Include a read-only doctor check for process liveness, build/version, owned port or session, and required authentication. Capture both action and resulting state, including external side effects when authorized; do not substitute internal setters for the real user path. For dry-run or test modes, verify which side effects are actually skipped rather than trusting the name. Document every helper invocation and required executable permission. Do not leave speculative commands or selectors as working instructions.
3. Seed an indexed map of roughly three to five important features, with each feature’s subfeatures, user entry paths, exact drive recipe, observable acceptance criteria, and prerequisites/gotchas. A later proof must account for all relevant mapped entry paths.
4. With required execution permission, prove one mapped feature end to end and retain the evidence after cleanup. Exercise launch, doctor, one mapped feature, evidence capture, and cleanup end to end. Clean failed attempts too. Stop only instances this run owns; never kill by process name. Verify the evidence survives final cleanup and label unexecuted instructions as a draft.
5. If the generated instructions cannot be executed with the available capability and required permission, label the result a draft and state the exact unverified steps.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-maintain-verification-skill](../pstack-maintain-verification-skill/SKILL.md)
- [pstack-principle-prove-it-works](../pstack-principle-prove-it-works/SKILL.md)

## Source

Adapted from [pstack/skills/create-verification-skill/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/create-verification-skill/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
