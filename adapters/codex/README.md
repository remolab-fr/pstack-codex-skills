# Codex host adapter

Read the [portable contract](../../core/contract.md) and [capability definitions](../../core/capabilities.md). This text maps portable intent to the active host. It does not create tools, credentials, permissions or settings.

## Identify the actual Codex surface

Codex CLI/IDE, Codex Cloud and a hosted assistant embedding the Codex harness expose different tools. Select the surface from the actual session, not the repository name. Do not require hosted-assistant APIs in an ordinary Codex session, and do not assume a CLI command is available in a hosted session.

- **Local Codex CLI/IDE:** use the current authorized workspace and its exposed file, shell and patch tools. Respect applicable `AGENTS.md`, sandbox roots, network policy and approval controls. A separate hosted task-creation service is not a prerequisite for local work.
- **Codex Cloud:** use the task's selected environment and available tools. A local path on another machine is not available unless transferred through an authorized route.
- **Hosted assistant:** follow that host's environment selection, task creation, messaging and connector rules when those capabilities actually exist. Do not translate them into fictional standard Codex APIs.

Tool names and argument schemas come from the running session. Capability names in this repository are conceptual, not literal tool calls. No instruction here changes sandbox settings, approval policy, account access or managed requirements. An inaccessible operation remains blocked; never disable protections to make a procedure work.

## Repository source versus account installation
The skills in this repository are source artifacts. They are not automatically installed or enabled by a push or clone. A host may allow explicitly reading a skill at its repository path. Keep the whole repository available so relative contract, adapter and workflow links resolve. Resolve a symlinked skill to its physical directory before following relative links. Individual skill folders depend on shared repository files and must not be distributed alone.

Personal installation is a separate user-authorized operation using the active host's canonical skill-management instructions. Do not substitute a scratch copy for that installation, guess an installation directory, or claim that a repository file is an enabled account skill. Package required linked resources when using a different destination. For local Codex, the [documented discovery locations](https://learn.chatgpt.com/docs/build-skills) include `.agents/skills` within repositories and `$HOME/.agents/skills`; symlinked skill folders are supported. The [repository installation instructions](../../README.md) retain the complete checkout. These local paths do not imply account-wide installation in a hosted app.

## Source and integration discovery
Discover the actual tools and connected plugins in the session. Prefer a connected provider tool for supported actions. Distinguish a listed tool, a working account connection, access to the exact repository/document, and permission for a write.

Map source.read/search and forge.read/checks/reviews to a suitable available connector. Use an authorized execution environment only when a connector cannot provide the needed operation. Git and provider CLIs are optional capabilities, never assumed dependencies. Do not install them implicitly.

Map external writes separately: publishing a branch, creating a PR, posting a comment, retargeting, merging and enabling auto-merge are distinct effects. Re-read exact current state before consequential writes and verify the result after them.

## Environments and app control
Respect an explicitly requested environment. Otherwise follow the host's current environment selection rules. In a hosted assistant that requires a task-creation route for the user's computer or saved environments, use that route. In a local CLI/IDE session already running in the authorized workspace, use its native tools directly within its sandbox. Do not switch machines to evade a denial.

Inspect actual connection and attachment requirements. A chat app surface is not evidence of computer access. Use the host's supported browser or app tools and identify which browser/environment is being used. App checks require safe fixture state and authorization for side effects.

## Delegation and models
Use native collaboration workers only where permitted for the task. Otherwise use host task threads for selected remote/local environments. Bound concurrency by actual capacity and preserve one writer per mutable artifact.

Resolve explorer, implementer, reviewer and synthesizer roles to available permitted models. Inherit the current model by default. Do not copy upstream vendor names, guess a replacement slug, or silently change reasoning budgets. Host instructions govern model overrides and worker lifetime. Describe independent same-model reviews honestly when a different model is unavailable.

A child that inherits connectors can still have write tools even if its prompt says read-only. Benny's isolation-dependent execution requires a verifiable technical boundary. If missing, block that portion; do not fall back to an equally privileged coordinator.

## History and evidence
Use a supported history interface when exposed, the current conversation, or a supplied authorized handoff/export. A general personal-context search tool is not assumed. In local Codex, the user can resume an existing session through the documented client interface; do not reconstruct it by reading private session storage. Scope retrieval to the requested task and time window. Do not scan protected internal session files, private host state or unrelated project transcripts.

Decision logs contain public rationale, evidence and outcomes. They are not transcripts of hidden deliberation. Follow actual sharing permissions for artifacts and conversations.

## Communication, secrets and automation
Reply through the active client. Use a dedicated user-message tool only when the host exposes and requires one; ordinary CLI/IDE responses use the conversation directly. Do not copy upstream UI navigation or assume slash commands, modes, confirmation widgets or secure-secret forms exist.

Secrets must use a verified host-supported handoff. Never ask for credentials in chat, print them, or copy them from private credential files. If the provider requires new persistent access or network/security changes, apply the host's specific approval requirements.

Future/recurring work requires the user's bounded schedule/event request, destinations and action scope. Prepare Benny as disabled until those are configured and verified. Continuing an already requested in-progress task is not authority to create a new recurring automation. Codex CLI and the IDE extension do not provide the Scheduled management interface. If no authorized scheduling capability exists, return a disabled plan for a supported client; do not silently create cron jobs, background daemons or CI workflows.

## Capability outcomes
For each required operation, report available, unsupported, disconnected, denied or unknown based on evidence. Do not treat unavailable native integrations as a broken portable workflow. Offer a useful scoped draft or analysis where possible; preserve the blocker for the unavailable effect.

## Official documentation baseline

Checked 2026-10-07. Capability availability still depends on the installed client, account and session.

- [Build skills: discovery, invocation and symlinks](https://learn.chatgpt.com/docs/build-skills)
- [Codex CLI: local execution and session continuation](https://learn.chatgpt.com/docs/codex/cli)
- [Subagents: delegation and model inheritance](https://learn.chatgpt.com/docs/agent-configuration/subagents)
- [Agent approvals and security](https://learn.chatgpt.com/docs/agent-approvals-security)
- [Scheduled tasks: supported surfaces](https://learn.chatgpt.com/docs/automations)
