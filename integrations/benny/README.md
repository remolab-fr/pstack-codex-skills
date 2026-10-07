# Benny operational reference

These procedures are inactive. No automation, service connection, ticket, PR or message is created by this repository.

1. Read [setup-benny](procedures/setup-benny/PROCEDURE.md)
2. Prepare a private, secret-free configuration using [configuration.example.json](templates/configuration.example.json)
3. Resolve provider capabilities, exact destinations, safe testing and actual isolation
4. Obtain the required authorization before creating schedules or external writes
5. Use [triage](procedures/triage-issue-reports/PROCEDURE.md) and [reproduction](procedures/reproduce-and-fix-issues/PROCEDURE.md) only in that configured scope

The templates are examples, never authorization. Keep account credentials out of configuration and worker prompts. If code execution cannot be technically isolated from Slack credentials/write tools where required, block that execution instead of substituting a credentialed coordinator.

User-owned configuration, routing and feature maps live outside the distributed procedure directory. Refreshes must preserve them and any local changes.

Before enabling, resolve every required null field for the chosen workflow. Configure unique terminal verdict markers and the trusted sender identity; markers are evidence selectors, not permission. Optional operations posts, evidence uploads and bounded rejection/follow-up windows remain off unless their destinations, retention, budgets and actions are explicitly approved. Read back test posts under the exact source parent, and run the authorized safe control smoke test before reproduction. No executable configuration loader or scheduler is shipped.
