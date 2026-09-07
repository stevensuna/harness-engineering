# Harness Engineering

This guide is for agents consuming the corpus. Use the repository as shared
context for applying Ryan Lopopolo's harness-engineering work to another task,
system, or repository. When this repository is supplied as context for another
target, treat it as read-only. When a task explicitly targets this repository,
follow [`docs/AGENTS.md`](docs/AGENTS.md) for public prose and
[`sources/AGENTS.md`](sources/AGENTS.md) for source material. Follow
[`playbooks/AGENTS.md`](playbooks/AGENTS.md) when using or editing a playbook.

## Application routing

- Read [`playbooks/README.md`](playbooks/README.md) before selecting a
  repository-authored procedure.
- To learn or teach the practice, read [`README.md`](README.md) and the thesis
  index in [`docs/README.md`](docs/README.md).
- To improve the harness around one observed job, read
  [`playbooks/improve-harness.md`](playbooks/improve-harness.md) after the
  target's instructions and before collecting a baseline or making a change.
  Use thesis routing inside its gap-classification step.
- To assess a repository broadly, read
  [`playbooks/repository-review.md`](playbooks/repository-review.md) before
  beginning the review.
- To make a comparative, causal, or longitudinal claim, read
  [`evals/README.md`](evals/README.md) before running conditions.

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
