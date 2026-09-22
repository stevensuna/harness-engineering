# Harness Engineering

This guide routes agents through the corpus. When it is context for another
target, keep it read-only. When the task edits this repository, use the nested
guide for the files being changed.

## Application routing

- Use [`README.md`](README.md) and [`docs/README.md`](docs/README.md) for
  orientation, the matching playbook for an application, and `evals/` only for
  comparative claims. Load those pages when the task needs them.
- For a new or missing development environment, use
  [`playbooks/worktree-bootstrap.md`](playbooks/worktree-bootstrap.md).

For other target-specific work, do not preload application guides or the thesis
corpus; use the unresolved-decision routing below.

## Context routing

Use target-local evidence first. When a consequential decision remains open,
read one matching thesis README; add a second only for a distinct concern.
Follow cases or sources only when their evidence can change the decision.
The target's contracts govern adaptation and verification.

| Unresolved decision | Route |
| --- | --- |
| Worker capability, task-size assumptions, instruction or tool semantics | [Fixed worker](docs/fixed-worker/) |
| Private changing operating knowledge and user-facing domain outcomes | [Last-mile deployment](docs/last-mile-deployment/) |
| Whole-job ownership, delegation, and lifecycle closure | [Whole job](docs/whole-job/) |
| Progressive disclosure, skills, runbooks, and context curation | [Just-in-time context](docs/just-in-time-context/) |
| Capability gaps versus tool discovery, invocation, or interpretation | [Tool legibility](docs/tool-legibility/) |
| Domain ownership, nonfunctional requirements, and canonical data boundaries | [Domain modeling](docs/domain-modeling/) |
| Consequential mutation scope, approval, credentials, audit, and recovery | [Authority](docs/authority/) |
| Claim-matched evidence and artifact identity across build, test, release | [Proof](docs/proof/) |
| Failed trajectories, recovered principles, and harness drift | [Feedback](docs/feedback/) |
| Dependencies, coherence, lifetime risk, migration, and proportionality | [Durable systems](docs/durable-systems/) |
| Recurring loops, owned state, distillation, and gardening | [Continuous maintenance](docs/continuous-maintenance/) |
| Human attention, outcomes, utilization, and economics | [Effectiveness](docs/effectiveness/) |

For public-post evidence, use
[`sources/twitter/README.md`](sources/twitter/README.md) as the human index and
query the adjacent JSON corpus for captured text and canonical links. Use
[`sources/sources.json`](sources/sources.json) for source provenance.

When the task needs Ryan's full argument or original language, follow the local
text links in the [source library](sources/README.md). The repository preserves
his hyperbo.la articles so an agent does not depend on web access to read them.

For attribution, chronology, or related-work questions, consult
[`docs/lineage/`](docs/lineage/) and the source manifest.

## Environment qualification

Before running a repository job, inspect its toolchain pins, package manifests,
lockfiles, setup scripts, and available native checks. Prefer the pinned
runtime and project-local executables. In a fresh Git worktree, install the
declared dependencies with the lockfile before diagnosing missing commands;
ignored directories such as `node_modules` are not copied by Git. Verify the
runtime and one representative native check, then inspect their output.

For implementation work, completion means the requested change is implemented,
the relevant checks have run in the qualified environment, their output has
been inspected, failures caused by the change have been fixed, and the checks
have been rerun. If a check remains blocked, record the exact command, error,
and unverified boundary instead of treating installation or source inspection
as proof.
