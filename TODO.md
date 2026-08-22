# TODO — Stirling PDF (fork)

> Deliberately plain `-` bullets, never `- [ ]` checkboxes. A column-zero checkbox in a
> TODO.md is the dev-system dispatcher's input queue and would spawn an unattended build.
> Promoting an item to a checkbox is a deliberate act.

## Findings (non-blocking; logged, not fixed)

- **`engine/.env` is tracked in git and carries a live PostHog analytics key.** It is a
  `phc_`-prefixed *public project key* - the kind designed to be embedded in client code,
  write-only, cannot read data - and it comes from upstream's public repository, so it is not
  a secret leak. Worth swapping for our own key before any deployment, so our document
  analytics do not report into upstream's project. Path only, value never recorded.

- **The Python "engine" installs its packages but creates no `engine/.venv`.** `task
  engine:install` exits 0 and reports ~220 packages installed, yet only `.venv-pre-commit`
  exists on disk. Harmless today because nothing runs the engine, but `task dev:all` will
  need this resolved. Re-check where `uv sync` placed the environment.

## Backlog

- Decide whether this fork deploys (Coolify) or stays local-only, and fill in the
  `## Deployment` section of CLAUDE.md either way.
- Fill in the `Roles / actors` section of CONTEXT.md once account handling is configured.
