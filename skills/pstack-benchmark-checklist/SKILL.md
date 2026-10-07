---
name: pstack-benchmark-checklist
description: "Use when the user requests benchmark checklist or its workflow. Define the claim and baseline before measuring."
---

# Benchmark Checklist

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

1. Define the claim and baseline before measuring. Read the actual harness before running: identify the timed interval, counted work, ignored errors, and how asynchronous or lazy work is awaited or consumed. Check machine load and generator saturation; disclose unavoidable competing workloads and interleave conditions. Choose measurement depth before running. A user-requested rough ballpark may use one explicitly labeled run, but still check output correctness, errors, and actual timed work. Choosing an implementation is not a ballpark.
2. Check the limiting resource, comparable production settings, theoretical bounds, failures and output correctness, repeatability, end-to-end relevance, and whether the intended work occurred inside the timed interval. Profile separately from reported timings. Name the limiter from a separate profile or runtime counters and connect it to source. Calculate physical throughput bounds and the maximum end-to-end benefit from the changed fraction; an implausible speedup is evidence of skipped work, caching, or a faulty measurement.
3. Alternate conditions and use at least five samples per condition where practical.
4. A difference below run variability is inconclusive; an untuned comparison cannot choose an implementation winner. Also mark a comparison inconclusive if its claimed difference lacks evidence about the limiter, failure counts, or whether the timed work occurred. Report median, range, versions, workload, errors and raw evidence.

## Completion and evidence

- Return the requested result or a precise partial/blocked outcome
- Cite the actual source, artifact, revision or observable check supporting material claims
- State uncertainty, inaccessible sources and tests not run
- Keep implementation, publication and installation status distinct

## Boundaries

Apply this procedure only inside the requested task. Do not infer permission to post, merge, delete, install dependencies, access another environment, modify credentials or create recurring work. Preserve user work and legal/security requirements. The shared contract takes priority over an aggressive interpretation of any step.

## Related procedures

- [pstack-principle-explain-the-number](../pstack-principle-explain-the-number/SKILL.md)

## Source

Adapted from [pstack/skills/benchmark-checklist/SKILL.md](https://github.com/cursor/plugins/blob/d0ef80d86795816da932a153458c5dbe192d294e/pstack/skills/benchmark-checklist/SKILL.md).
This is a rewritten portable procedure, not a literal copy of the source's host-specific behavior.
Copyright (c) 2026 Lauren Tan. MIT license; see [LICENSE](LICENSE).
