# GTA RP Server

Canonical repository and Source of Truth for the GTA RP Server project.

The project is a long-lived custom game product built on FiveM/Cfx.re. It is not a collection of unrelated FiveM scripts. Product architecture, documentation, source code, infrastructure, and project resources will evolve in this repository.

## Current state

The repository is being initialized. The first project document is the [Project Charter](docs/project/PROJECT_CHARTER.md), currently in `DRAFT`.

No document should be treated as an approved decision unless its status is explicitly `APPROVED`. Significant technical decisions are recorded as ADRs.

## Repository layout

- `docs/` — project, architecture, ADRs, standards, and specifications.
- `resources/` — future FiveM resources.
- `apps/` — future web applications and supporting services.
- `packages/` — future shared packages.
- `infrastructure/` — future deployment and operational configuration.

Directories are created when they gain real content; the repository intentionally avoids placeholder-file clutter.

## Working principles

- Repository-first: review current relevant `APPROVED` documents before significant design or implementation work.
- Critical gameplay logic is server-authoritative; clients and NUI are untrusted.
- Qbox is replaceable infrastructure, not the owner of product domain architecture.
- Design for long-term maintainability, security, and a realistic path to 1000+ concurrent players.
- Change approved decisions explicitly through review and, when appropriate, a new ADR.
- Prefer branch → pull request → review → merge for significant changes.

See [Documentation](docs/README.md) for the documentation map and lifecycle.
