# Design Backlog

This backlog tracks documentation and design work that is known to be needed but is not yet an accepted decision. Backlog entries are not architecture approval.

## Current queue

| Priority | Deliverable | Initial scope | Status |
| --- | --- | --- | --- |
| 1 | `docs/project/PROJECT_CHARTER.md` | Review and approve product purpose, boundaries, constraints, and success direction | `DRAFT` |
| 2 | `docs/architecture/ARCHITECTURE.md` | Define the high-level product and platform architecture without binding domain logic to Qbox | `PLANNED` |
| 3 | Initial ADR set | Record Enhanced-first, Qbox as a replaceable platform layer, and the server-authoritative model for review | `PLANNED` |
| 4 | `docs/architecture/DOMAIN_MAP.md` | Establish bounded domains, ownership, and cross-domain interaction rules | `PLANNED` |
| 5 | `docs/architecture/DATA_ARCHITECTURE.md` | Define persistence ownership, integration boundaries, migrations, auditability, and data access rules | `PLANNED` |
| 6 | `docs/architecture/SECURITY.md` | Define the threat model and server-side validation requirements | `PLANNED` |
| 7 | `docs/architecture/PERFORMANCE.md` | Define performance budgets, measurement practices, and 1000+ player scalability constraints | `PLANNED` |
| 8 | Repository architecture | Define the concrete layout for resources, apps, packages, infrastructure, tooling, and ownership | `PLANNED` |
| 9 | `docs/standards/DEVELOPMENT_STANDARD.md` | Establish development, testing, review, migration, and observability standards | `PLANNED` |
| 10 | `docs/standards/AI_DEVELOPMENT_STANDARD.md` | Establish mandatory boundaries and verification rules for AI coding agents | `PLANNED` |

## Later domain specifications

Domain specifications should begin only after the foundational documents above provide enough boundaries. Candidate areas include Characters, Economy, Jobs, Factions, Vehicles, Property, Justice, Inventory, and Administration.

The first implementation milestone should be a small vertical slice that validates the architecture end to end, rather than a broad collection of disconnected features.

## Backlog rules

- Add an item when the work is real and has a clear outcome.
- Do not treat `PLANNED` or a backlog entry as an accepted decision.
- Do not create empty documents simply to mirror this list.
- When work starts, create the document with status `DRAFT` and link it from `docs/README.md`.
- Use an ADR for a significant technical decision and preserve the history of superseded decisions.

