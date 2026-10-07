# pstack for Codex

**51 skills to help Codex plan, build, review, and test software.**

A skill is a Markdown file with steps for a task. These skills help Codex check the evidence, work within your request, and explain what is done or blocked. They adapt [pstack](https://github.com/cursor/plugins/tree/d0ef80d86795816da932a153458c5dbe192d294e/pstack) for Codex.

## Start here

### 1. Check what you need

- Codex CLI or IDE extension with local skill support
- macOS, Linux, or WSL, with Git and a POSIX shell
- Internet access to clone the public repository over HTTPS

### 2. Install the skills

Run this command in your terminal. It downloads the repository and links all 51 skills to your local Codex skills folder.

```sh
(
  set -eu
  repo="$HOME/.local/share/pstack-codex-skills"
  dest="$HOME/.agents/skills"
  mkdir -p "$(dirname "$repo")" "$dest"
  git clone https://github.com/remolab-fr/pstack-codex-skills.git "$repo"
  for skill in "$repo"/skills/*; do
    target="$dest/${skill##*/}"
    if [ -e "$target" ] || [ -L "$target" ]; then
      printf 'Already exists: %s\n' "$target" >&2
      exit 1
    fi
  done
  for skill in "$repo"/skills/*; do
    ln -s "$skill" "$dest/${skill##*/}"
  done
)
```

The public HTTPS clone does not require a GitHub account, password, or token.

The files stay in `~/.local/share/pstack-codex-skills`. The links go in `~/.agents/skills`, so you can use the skills across projects on this machine. **Keep the whole repository.** Each skill uses shared files; copying only a `SKILL.md` file will break those references.

The command stops if the checkout is not empty or a skill path already exists. It does not overwrite existing skills. A failed attempt may leave folders behind; inspect them before trying again.

### 3. Try a task

In Codex CLI or the IDE extension, open `/skills` and look for `pstack-poteto-mode`. Restart Codex if it does not appear. See [OpenAI's skill discovery guide](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills).

Paste this into Codex:

```text
$pstack-poteto-mode Investigate why this test fails. Reproduce it and propose the smallest fix before editing.
```

Replace “this test” with your test name or failure details. `pstack-poteto-mode` helps choose a workflow. For a specific job, choose a skill directly:

```text
$pstack-architect Compare two designs for this API change. Recommend one and explain the migration steps.
```

```text
$pstack-interrogate Review the current diff for bugs, regressions, and missing tests. Report findings without editing files.
```

```text
$pstack-tdd Fix this bug with a regression test. Run the relevant checks. Do not publish or merge.
```

## Which skill should I use?

| I want to… | Use |
| --- | --- |
| Choose a workflow | [pstack-poteto-mode](skills/pstack-poteto-mode/SKILL.md) |
| Explore the available skills | [pstack-poteto-help](skills/pstack-poteto-help/SKILL.md) |
| Plan a design or migration | [pstack-architect](skills/pstack-architect/SKILL.md) |
| Review a change | [pstack-interrogate](skills/pstack-interrogate/SKILL.md) |
| Find affected code and risks | [pstack-blast-radius](skills/pstack-blast-radius/SKILL.md) |
| Fix a bug with a test | [pstack-tdd](skills/pstack-tdd/SKILL.md) |
| Write clear documentation | [pstack-technical-writing](skills/pstack-technical-writing/SKILL.md) |

The [full catalog](CATALOG.md) lists all 51 skills. Installing them does not run them all. Use an explicit skill name if Codex does not select the one you need.

## What to expect

Skills guide Codex using the tools and permissions it already has. They do not add account access, models, browser tools, or background jobs. If a required tool is missing, the task must stop at that step or use an allowed alternative.

Installing here affects this machine only. It does not install skills in cloud tasks or other devices. For cloud and hosted environments, read the [Codex adapter](adapters/codex/README.md).

Reading or installing a skill does not give permission to publish, merge, send messages, delete data, or set up services. The [execution contract](core/contract.md) applies to every workflow.

**Test status:** file structure, metadata, links, and a temporary installation layout have been checked. Live Codex skill discovery and complete workflows have not been tested. See [VALIDATION.md](VALIDATION.md) for the checks and remaining limits.

## Update

Review the incoming changes, then update the checkout:

```sh
git -C "$HOME/.local/share/pstack-codex-skills" pull --ff-only
```

Existing links use the updated files immediately. New skill folders need new links. If Git reports a conflict or a diverged branch, preserve your local changes before resolving it.

If you installed a private copy before the public launch, its history is replaced by a fresh public history. Preserve any local edits, move the old checkout aside, and clone the public repository at the same path. Existing symlinks then resolve to the new checkout. Do not merge the old private history into the public branch.

## Remove

Remove only the symlinks in `~/.agents/skills` that point into `~/.local/share/pstack-codex-skills/skills`. Keep other skills and real directories. You can then move the checkout to Trash. Restart Codex if removed skills still appear.

For one-project use, put the links in that project's `.agents/skills` instead. Keep the complete checkout. Avoid duplicate skill names across both locations, and do not commit machine-specific absolute symlinks.

## Repository guide

| Path | Contents |
| --- | --- |
| [skills/](skills/) | 51 skills and their license notices |
| [workflows/](workflows/) | 23 task playbooks |
| [core/](core/) | Shared scope, capability, and evidence rules |
| [adapters/codex/](adapters/codex/) | Guidance for each Codex environment |
| [roles/](roles/) | 2 role profiles for delegation |
| [integrations/benny/](integrations/benny/) | 3 inactive procedures and configuration templates |
| [provenance/](provenance/) | Upstream revision and source inventory |
| [scripts/](scripts/) | Development checks for packaging and repository content |

The skills are a text-only adaptation. Upstream executable helpers, hooks, dependency installers, MCP servers, and CI workflows are not included. This repository's development checks and CI validate the distribution; they do not execute skills or activate integrations. The [adaptation notes](docs/adaptation.md) explain the changes. The [source inventory](provenance/source-inventory.json) accounts for all 164 upstream files.

## Contribute and report problems

Read [CONTRIBUTING.md](CONTRIBUTING.md) for changes and bug reports. For a security issue, follow [SECURITY.md](SECURITY.md) before sharing details. Maintainers preparing a public release can use the [release checklist](docs/releasing.md).

## License and credits

[MIT](LICENSE). Adapted from pstack by Lauren Tan, with the original copyright notice preserved. This is an independent project, not an official Cursor plugin or OpenAI product. See [NOTICE.md](NOTICE.md) for attribution.
