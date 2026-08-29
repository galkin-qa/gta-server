# Project Charter

**Status:** `DRAFT`

This charter is the first repository-native statement of project intent. It is open for review and does not have the authority of an `APPROVED` document.

## Product intent

Build a long-lived, high-realism GTA V roleplay product on FiveM/Cfx.re. The product is its own game platform—its systems, data, UX, economy, world rules, and content—not a bundle of unrelated FiveM scripts.

GTA V Enhanced is the target platform. A possible GTA VI product would be a separate server/product rather than a migration target for this one.

## Product direction

- One primary game world/server.
- Small initial population with a gradual goal of 1000+ concurrent players within one to two years.
- Quality, architecture, stability, security, and long-term maintainability take priority over the fastest possible MVP.
- Early differentiation focuses on UX, UI, coherent game systems, world consistency, and polish.
- Custom 3D assets, vehicles, animations, sounds, and world content grow incrementally rather than blocking early gameplay development.
- The initial third-party service/resource budget is approximately 10,000 RUB per month and may grow with the product.

## Product scope

The long-term product includes:

- FiveM gameplay systems and a persistent roleplay world;
- a realistic but playable economy;
- characters, jobs, government factions, player organizations, families, vehicles, property, justice, inventory, administration, and related systems;
- custom NUI and a shared design direction across player-facing surfaces;
- a website, personal cabinet, forum integration, Discord integration, and other web resources;
- a platform API separating web applications and integrations from FiveM/Qbox internals.

Detailed domain boundaries are intentionally deferred to `DOMAIN_MAP.md` and subsequent specifications.

## Foundational constraints

The following constraints restate the current project baseline; they do not replace the future APPROVED architecture or ADRs:

- Critical game operations are server-authoritative. Client and NUI input is untrusted and must be validated server-side.
- Qbox is a replaceable infrastructure dependency, not the product domain architecture. Domain systems should interact through project-owned interfaces and adapters rather than pervasive direct Qbox coupling.
- Architecture must provide a realistic path to 1000+ concurrent players while avoiding premature distributed systems and abstraction without practical value.
- Security, auditability, performance, and observability are design concerns from the beginning.
- Core domains own their data; one domain must not directly mutate another domain's internal data.
- Significant monetary operations require an auditable transaction/ledger model rather than a single mutable balance as the architectural foundation.
- Third-party resources require evaluation for quality, support, compatibility, performance, licensing, escrow restrictions, and replaceability.
- The repository is the Source of Truth. Significant changes use branch, pull request, review, and explicit documentation updates.

## Current technology baseline

Until reviewed and superseded through repository documentation and ADRs:

- Platform: FiveM/Cfx Server, GTA V Enhanced-first.
- Base framework: Qbox, treated as replaceable infrastructure.
- Gameplay scripting: Lua 5.4 / CfxLua.
- NUI: React, TypeScript, and Vite.
- Web ecosystem: React/TypeScript; Next.js requires a confirmed architecture decision.
- Platform backend/API candidate: TypeScript and NestJS.
- Database: MariaDB; FiveM database access through oxmysql.
- Mature ox ecosystem components may be used where appropriate and replaceable.

This list is a baseline for future review, not permission to bypass ADRs or detailed design.

## Delivery principles

- Use repository-first design and review relevant `APPROVED` documents before significant work.
- Prefer a small vertical slice that tests the complete architecture over a wide set of disconnected MVP features.
- Measure performance rather than guessing and avoid global per-frame/per-tick work, unnecessary polling, and unnecessary broadcasts.
- Validate permissions, identity, ownership, prices, quantities, locations, replay/duplication risks, and persistent mutations on the server.
- Do not modify Qbox core without an exceptional, documented reason.
- Do not silently rewrite `APPROVED` decisions; propose and review the change and create an ADR when appropriate.

## Initial success direction

The first implementation milestone should demonstrate a coherent end-to-end player journey across identity, character entry, custom UI, one economic loop, persistence, and a personal-cabinet representation. Exact scope and acceptance criteria require later architecture and specification work.

## Open review work

Before this charter can become `APPROVED`, review must confirm:

- product boundaries and explicit non-goals;
- measurable success criteria for the first milestone;
- ownership and decision-making roles;
- risk priorities and budget assumptions;
- alignment with the initial architecture and ADR set.

Tracked follow-up work lives in [Design Backlog](../DESIGN_BACKLOG.md).
