# Validation and compatibility

Reviewed for public release on 2026-10-07.

## Run the checks

From the repository root, with Python 3.9 or newer:

```sh
./scripts/check
```

The checker uses only the Python standard library. It reads repository content and creates disposable packaging fixtures in the system temporary directory. It does not contact services, install skills in a real discovery directory, or execute skill instructions.

[GitHub Actions](https://github.com/remolab-fr/pstack-codex-skills/actions) runs the checker and a fully redacted Gitleaks scan of Git history on pushes and pull requests. The [workflow](.github/workflows/check.yml) uses read-only repository permissions, disables checkout credential persistence, pins the checkout action by commit, and verifies the downloaded Gitleaks archive against a pinned SHA-256 checksum. Upstream executable helpers remain excluded; this development tooling validates the distribution.

For a local secret scan with Gitleaks 8.30.1 installed:

```sh
gitleaks git --redact=100 --no-banner --timeout 60 --log-opts=--all .
gitleaks dir --redact=100 --no-banner --timeout 60 .
```

Secret scans and packaging checks are separate checks. Passing one does not imply the other passed. Do not add suppressions merely to obtain a green result.

## Packaging evidence

The release preparation checks passed for 51 skills, 23 workflow playbooks, 3 inactive Benny procedures, 2 role profiles, and 164 upstream inventory entries:

- Skill names and quoted descriptions parse and match their directory names; duplicate names and catalog IDs are rejected.
- Skill licenses match the root MIT license, and required contract and adapter links remain present.
- Catalog targets match the distributed files; JSON parses; source metadata, source hashes and mapped destinations agree between provenance records.
- Every inventory entry has a unique source path, a blob hash, a byte count, and an explicit adaptation or omission disposition.
- Internal Markdown file links resolve within the checkout. Link fragments and remote URL availability are outside this local check.
- Benny remains disabled, its action permissions remain false, and its example does not assert verified worker isolation.
- Temporary symlinks for all 51 skills resolve their shared resources from physical checkout locations, including paths with spaces.

Failure-path checks in disposable copies rejected malformed JSON and schema types, invalid frontmatter, broken links, altered license notices, enabled Benny actions, duplicate catalog or inventory entries, and missing mapped destinations. The documented installation command was separately tested for normal and spaced paths, an existing skill directory, a dangling symlink, and a nonempty checkout; conflict cases preserved existing files.

The Actions workflow passed `actionlint`, and the proposed changes passed `git diff --check`. CI execution must be checked on the exact published commit through the Actions page; local linting is not a CI result.

## Publication and provenance review

Before replacing the private history, the four original commits were reviewed as text and scanned with Gitleaks. The current source files were also scanned. No secrets were detected. This is a bounded review, not a guarantee that all sensitive data is absent. Original author and committer metadata is excluded from the fresh public lineage, whose commit uses a GitHub noreply identity.

A separate live read of the pinned [upstream tree](https://github.com/cursor/plugins/tree/d0ef80d86795816da932a153458c5dbe192d294e/pstack) verified all 164 inventory paths, hashes and sizes, the 51 skill source hashes, the subtree hash in [NOTICE.md](NOTICE.md), and the original MIT license bytes. [Source inventory](provenance/source-inventory.json) records adaptation decisions. Required upstream attribution stays intact when repository history is replaced.

Source review does not cover every repository surface. The [release checklist](docs/releasing.md) includes branches, tags, issues, pull requests, artifacts, release assets, visibility, public cloning, and private security reporting. Existing private clones must be preserved or removed by their owners; replacing this repository cannot erase copies held elsewhere.

## Compatibility limits

The instruction review distinguishes local CLI/IDE, Codex Cloud, and hosted assistants. Shared [contracts](core/contract.md) keep scope, capability availability, authorization, worker isolation, and evidence explicit. The [adapter](adapters/codex/README.md) records the official documentation baseline and the required behavior when a tool is unavailable.

Live Codex discovery or automatic skill selection, browser operation, external account access, tracker writes, PR monitoring or merging, webhook delivery, scheduling, account-specific models, and complete workflow execution remain untested. Static validation and temporary installation fixtures do not establish those capabilities. No exact behavioral equivalence with omitted upstream executable helpers is claimed.

After any change, run the checker and secret scan, review the actual instructions, and inspect CI for the exact revision. Validate live behavior only in an explicitly authorized target environment.
