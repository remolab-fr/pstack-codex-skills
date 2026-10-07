---
name: pstack-typescript-best-practices
description: "Use when the user requests typescript best practices or its workflow. Follow the repository's TypeScript configuration and conventions."
---

# Typescript Best Practices

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

The requested artifact or change, relevant source/revisions, acceptance criteria, constraints and authorized output destination.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. Follow the repository's TypeScript configuration and conventions. Treat unparsed external values as unknown. Prefer the repository’s schema validator and inferred types over duplicate interfaces or unverified hand-written type guards; a guard must actually establish every property it claims.
2. Model semantic states explicitly, validate external data at boundaries, avoid assertions that hide uncertainty, and make variant handling exhaustive. Use discriminated unions, semantic brands where interchange would be a bug, exhaustive never cases, and satisfies where supported. Prefer narrowing and validation over casts. Derive types with existing schemas or standard utility types rather than hand-maintained parallel definitions. Choose constructive representations, such as a head plus rest for nonempty data, only where an operation would otherwise be partial. Do not strengthen types merely for precision when the ordinary type already supports total functions.
3. Prefer types derived from authoritative schemas, coherent ownership and small interfaces. Keep runtime validation where external values enter.
4. Favor named object parameters when they clarify calls, while respecting real hot-path constraints. Use structured diagnostics with useful identifiers; exercise real framework primitives and disposal/leak checks where available instead of mocking locally runnable behavior.
5. Verify against the project's supported compiler and test commands rather than assuming the newest language features.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Source

Adapted from [pstack/skills/typescript-best-practices/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/typescript-best-practices/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
