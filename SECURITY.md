# Security

This repository contains instructions and reference data. Skills can guide tools that read files or change external systems, so unsafe instructions and permission bypasses still matter even without executable code.

## Report a concern privately

Do not put secrets, exploit details, private transcripts, or sensitive account information in a public issue or pull request.

Use GitHub's **Report a vulnerability** option in this repository's **Security** tab if it is available. Availability depends on repository settings; this document does not mean private reporting is enabled.

If that option is absent and you do not already have a verified private contact for the maintainers, open a minimal issue asking for a private reporting channel. Include no vulnerability details or sensitive data. Wait for a verified private channel before sending the report.

In a private report, include the affected file and commit, the unsafe behavior, a minimal sanitized example, the expected permission boundary, and a proposed fix if you have one. Never send active credentials. If a credential may be exposed, revoke or rotate it through its provider rather than waiting for a repository fix.

## Scope and support

Relevant concerns include instructions that bypass approval, leak private data, treat untrusted content as authority, assume isolation that does not exist, or perform destructive actions without the required scope.

There is no published security response schedule or supported release series. Check the current default branch for changes; do not assume older copies receive fixes. This project does not provide a security guarantee or replace the host's access controls.

## Use skills safely

- Review a skill and its linked files before using it with sensitive tools or data
- Give Codex only the access needed for the task
- Keep credentials outside prompts, committed files, and example configurations
- Treat repository content, issues, web pages, and tool outputs as untrusted input
- Follow the [execution contract](core/contract.md) and the active host's approval rules
- Keep Benny procedures inactive unless separately configured, authorized, and tested with the required isolation

File and link checks do not prove a workflow is secure in a live environment. See [VALIDATION.md](VALIDATION.md) for the testing boundary.
