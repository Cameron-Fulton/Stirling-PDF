# Stirling PDF — Domain Glossary

> The vocabulary this project reasons in. Architecture and refactor work reads this file
> to use the project's own terms (not generic words like "service" or "handler"). When a
> deepening or feature names a new domain concept, add it here in the same session.
>
> Companion: `project-kb/adr/` — load-bearing decisions and rejections that future surveys
> should not re-litigate.

## Project intent
A self-hosted, open-source PDF platform: 50+ document operations (edit, merge, split, sign,
redact, convert, OCR, compress) exposed through a browser UI, a desktop client, and a private
API. The whole point is that documents are processed on infrastructure we control and are never
sent to a third-party service.

## Core entities
- **Tool** — one named PDF operation (merge, split, redact, OCR…). Each tool is registered on
  both sides: a backend endpoint that does the work and a frontend entry that renders its form.
  Adding one touches both halves — see the repo's own `ADDING_TOOLS.md`.
- **Pipeline** — a saved, ordered chain of Tools applied to a file or batch without writing code.
  This is the no-code automation surface, distinct from calling the API directly.
- **Flavor** — a build variant of the same codebase (for example the SaaS flavor referenced in
  `gradle.properties` and the Taskfile). Flavors change which features compile in, so a change
  that builds in one may not build in another.

## Modules
- **`app/`** — the Java/Spring Boot backend: tool endpoints, security, job handling.
- **`frontend/`** — the React + TypeScript client (also packaged as the Tauri desktop app).
- **`engine/`** — the document-processing layer the tools call into.
- **`devTools/` · `scripts/` · `testing/`** — build, lint, and test tooling; not shipped.

## Roles / actors
- **(to be filled)** — capture the real auth roles the fork uses once account handling is
  configured; the upstream project ships user accounts, invites, and per-tool access.

## Out-of-scope concepts
- **Sending documents to an external processing API** — deliberately not done. The privacy
  guarantee is the product; any feature that uploads a user's PDF off-box defeats it.
- **Contributing changes back upstream** — this is our fork. Pull requests target
  `Cameron-Fulton/Stirling-PDF`, never `Stirling-Tools/Stirling-PDF`, unless explicitly asked.
