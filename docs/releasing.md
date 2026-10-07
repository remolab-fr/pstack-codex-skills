# Public release checklist

This checklist prepares a release. It does not authorize changing visibility, publishing a package, or enabling a service.

## Before making the repository public

- [ ] Confirm the repository owner's approval of the exact repository and public release scope
- [ ] Review every branch, tag, and reachable commit, including commit messages, author names, and email addresses, for information that should stay private
- [ ] Review issues, pull requests, attachments, releases, artifacts, and other repository content that may become public; a source-file scan does not cover these surfaces
- [ ] Resolve any exposed credentials with their provider before release; deleting a file does not remove it from history
- [ ] Confirm the rights to distribute all included material; preserve [LICENSE](../LICENSE), [NOTICE.md](../NOTICE.md), and skill-level notices
- [ ] Check the upstream revision and per-file dispositions in [provenance](../provenance/)
- [ ] Verify a working private security-reporting route and update [SECURITY.md](../SECURITY.md) if needed
- [ ] Review repository description, topics, contribution settings, and any organization release requirements
- [ ] Run the checks in [VALIDATION.md](../VALIDATION.md) against the exact proposed revision and record their limits
- [ ] Run `./scripts/check` and the CI secret scan against the exact proposed revision
- [ ] Check the README's setup instructions in an authorized target Codex client before claiming live compatibility

Do not rewrite history, change security settings, create credentials, enable workflows, or install skills just to complete this checklist without the corresponding approval.

## At publication

- [ ] Get approval for any unresolved privacy or license decision
- [ ] Make only the approved visibility or release change
- [ ] Verify the public repository opens without authentication
- [ ] Verify the documented public HTTPS clone works; update the quickstart if changing its default transport
- [ ] Verify the intended files and commit are present and internal links still work
- [ ] If history was intentionally reset, verify the public branch has only the approved fresh history, review other exposed refs and repository surfaces, and tell existing users to preserve edits and re-clone
- [ ] State what was tested, what remains untested, and any known limitations in release notes

Publishing source does not install skills for users or activate integrations. A release tag, package, announcement, or new automation is a separate action.

A history reset replaces the published lineage; it does not revoke credentials or erase copies that other people already hold. Do not merge a prior private branch into the fresh public history. Keep any required private recovery copy outside the public repository.
