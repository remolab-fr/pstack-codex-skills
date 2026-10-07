# Contributing

Help make these skills clear, useful, and safe across Codex environments. Small fixes to instructions, examples, links, and portability are welcome.

## Report a problem

For a normal bug or suggestion, open a [repository issue](https://github.com/remolab-fr/pstack-codex-skills/issues). Include:

- The skill or file and the repository commit you used
- Your Codex client and relevant version, operating system, and available tools
- A small, sanitized example of the task
- What you expected and what happened

Remove credentials, personal information, private repository content, and account identifiers from examples and logs. For possible security issues, use [SECURITY.md](SECURITY.md) instead of posting details publicly.

## Propose a change

1. Read the [execution contract](core/contract.md), [Codex adapter](adapters/codex/README.md), and the files linked from the skill you want to change.
2. Fork the repository and make one focused change on a branch.
3. Keep instructions in simple English. State the required inputs, steps, evidence, and stopping condition. Explain missing-tool behavior.
4. Check the full procedure and its links, not only the edited sentence. Describe what you checked and what remains untested.
5. Open a pull request with the problem, the change, and your validation results. Do not include live credentials or private task transcripts.

Do not remove permission checks to make a workflow finish. A prompt cannot provide technical isolation or grant access. New integrations, runtime helpers, dependencies, and automatic actions need a separate design discussion. The installed skills contain instructions and reference data; repository development checks do not add runtime capabilities.

## Check your changes

Run the repository check from its root before opening a pull request:

```sh
./scripts/check
```

The check requires Python 3.9 or newer and uses only its standard library. CI runs repository checks and secret scanning. Use [VALIDATION.md](VALIDATION.md) to understand the evidence boundary and review the procedure itself:

- Skill names match their folders and have valid frontmatter
- Internal links resolve from the skill's physical checkout location, including when discovered through a symlink
- Shared contracts and capability checks remain present
- JSON parses; example integrations stay disabled and contain no secrets
- Catalogs, counts, and provenance match any added, moved, or removed files
- The root MIT license and each skill's license notice remain intact
- Examples are safe to copy and do not silently overwrite files or enable services

If you change setup commands, test them in temporary folders, including paths with spaces and existing-path conflicts. Do not use a real account's skills directory for a packaging test. Clearly distinguish static checks, simulated instruction walkthroughs, and authorized live tests.

## Attribution and rights

Only contribute material you have the right to share under this repository's [MIT license](LICENSE). Preserve existing copyright and license notices. Record new upstream sources, their revisions, and their license requirements in the relevant provenance records. See [NOTICE.md](NOTICE.md) for the current source.

Do not copy private prompts, customer data, internal notes, or third-party material without the necessary rights. Names of products describe compatibility and provenance; they do not imply endorsement.

## Working together

Be respectful and specific. Discuss the work, avoid personal attacks and harassment, and do not share another person's private information. Keep feedback constructive and make room for people with different backgrounds and levels of experience.
