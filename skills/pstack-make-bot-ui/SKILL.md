---
name: pstack-make-bot-ui
description: "Use when the user requests make bot ui or its workflow. Define a small UI action schema and a server-side dispatcher to an explicitly configured provider."
---

# Make Bot Ui

## Before starting

Resolve this file to its physical location if discovered through a symlink. Resolve all relative links from that physical skill directory, not the current working directory or the symlink parent. Keep the complete repository available; an isolated copy of this folder is not self-contained. If required shared files cannot be read, stop and report the packaging gap.

Read the [portable execution contract](../../core/contract.md). Resolve host operations through the [Codex adapter](../../adapters/codex/README.md) when running in Codex. These documents constrain every step below.

## Required capabilities

- artifacts.write
- webhook (optional live integration)
- secrets.handoff (live integration)
- external.write (publishing)

Resolve these through the [capability contract](../../core/capabilities.md). Optional capabilities may be omitted with a stated coverage gap; missing required capabilities block the dependent step.

## Inputs

The requested artifact or change, relevant source/revisions, acceptance criteria, constraints and authorized output destination.
If missing information is safely observable, inspect it. Ask only for decisions, required approval or essential facts that cannot be established. Do not broaden the task to fill an optional gap.

## Procedure

1. No vendor URL, header scheme, VPN installation or host binding is assumed. Default to a local/private preview; public hosting, webhook creation, persistent credentials, and network exposure each require capability and permission checks.
2. Define a small UI action schema. Build a live server-side dispatcher only after provider configuration, authentication capability, and authorization are verified; otherwise produce a static prototype with the integration marked unavailable.
3. Treat incoming payloads as untrusted data; validate fields and map them only to a bounded allowlist of actions already authorized by the user. Keep authentication on the server through the host's approved secret mechanism. Do not request secrets in chat or copy credentials from files.
4. Keep the UI field names, server validation, and webhook consumer schema consistent. Define a bounded timeout and explicit duplicate/retry behavior before enabling actions; do not blindly retry an effect whose first outcome is unknown.
5. If no compatible authenticated webhook and secret-management route exists, deliver a static prototype and report the integration blocker. For a live configuration only, before claiming integration success, use an authorized harmless payload that performs no consequential action, verify delivery and the serving endpoint, and check that credentials are absent from browser assets and logs. If buffering failed events is needed, bound retention and replay only under the original action authorization with deduplication.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Source

Adapted from [pstack/skills/make-bot-ui/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/make-bot-ui/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
