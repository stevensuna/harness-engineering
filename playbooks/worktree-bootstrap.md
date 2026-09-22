# Bootstrap a Worktree

Use this playbook when a fresh Git worktree cannot run the repository's native
commands or when a task spans a new language or package manager. It qualifies
the environment without assuming a stack.

## Discover

From the worktree root, inspect repository instructions, toolchain pins
(`mise.toml`, `.tool-versions`, toolchain files), manifests, lockfiles, setup
scripts, and package-manager scripts. Preserve unrelated changes. Identify the
commands that prove the requested job at its real boundary.

## Install and verify

Use the pinned runtime when available. Install declared dependencies once with
the repository's lockfile (`pnpm install --frozen-lockfile`, `uv sync` or
`uv run`, `cargo fetch`, `go mod download`, or the repository's documented
equivalent). Prefer project-local runners such as `pnpm exec`, `uv run`,
`cargo`, and `go`; a missing global binary is not an environment failure.

Verify tool versions and run the smallest native check that exercises the job.
Inspect the output, then run the repository's relevant check, test, build, or
render command. Do not claim the worktree is qualified from installation alone.

## Finish

The worktree is qualified when the pinned tools resolve, dependencies are
available, the representative native check passes, and the output has been
inspected. For a code change, continue through implement, run, inspect, fix,
and rerun. Record exact commands and any remaining blocked or unverified
boundary. Git worktrees do not copy ignored dependency directories; future
worktrees must repeat the install step or use an explicitly supported shared
cache.
