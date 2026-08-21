# Stirling PDF

> Read `D:/SYSTEM.md` first. It is the system constitution and overrides everything below.
> Project instructions are canonical in `AGENTS.md` (upstream-maintained) — read that next.

Self-hosted fork of Stirling PDF. Origin is `Cameron-Fulton/Stirling-PDF`; upstream is
`Stirling-Tools/Stirling-PDF` and is fetch-only. Never open a PR against upstream.

## Knowledge

- `CONTEXT.md` — domain glossary (Tool, Pipeline, Flavor, module map)
- `project-kb/work.md` — live edge; open tasks
- `project-kb/plan.md` — narrative, roadmap, delivered record
- `project-kb/index.md` — full map of `project-kb/`

**Agent write surface:** `project-kb/work-entries/` only. Never write directly to `work.md`
or `plan.md` — the reconciler compacts from `work-entries/`.

## Build

### Prerequisites (verified installed on this box 2026-08-21)

| tool | version | why |
|---|---|---|
| Temurin JDK | **25** | `build.gradle:54` sets `modernJavaVersion = 25`; CI uses `distribution: temurin`. Match the vendor. |
| Task | 3.53.1 | `Taskfile.yml` is the entry point; raw `gradlew`/`npm` skips wiring the tasks do. |
| uv | any | `task install` runs `engine:install`, which is `uv python install 3.13.8` + `uv sync`. **Not obvious from the stack description** - the engine layer is Python. |
| Node | 25.x | frontend `npm install` |

Gradle is NOT installed separately - the wrapper (`./gradlew`) fetches 9.7.1 itself.

Task-runner driven (`Taskfile.yml`), not raw Gradle/npm:

```bash
task install     # install backend + frontend deps
task dev         # run backend + frontend
task build       # build
task test        # test
task lint        # lint
task format      # format
```

## Deployment

N/A -- not yet configured. Update with the Coolify application UUID(s) and production URL(s)
when this fork is deployed. Coolify credentials live in `D:\.env` — never prompt for them.

## Git

- Remote must be `github.com/Cameron-Fulton/Stirling-PDF` — verify with `git remote -v` before any push.
- Never commit to `main`. Feature branches (`feat/`, `fix/`) only.
- `gh pr create` **must** pass `--repo Cameron-Fulton/Stirling-PDF --base main` explicitly;
  `gh` otherwise targets upstream, and a misfired PR is permanent.
