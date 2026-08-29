# Project Documentation

This directory is the index for the canonical project documentation in this repository.

## Source of Truth

GitHub is the Source of Truth for the current state of the project. Before significant architecture, game-system, security, performance, FiveM, Qbox, or technology work, review the relevant current documents in this repository, especially documents with status `APPROVED`.

If chat history, an old export, or memory conflicts with an `APPROVED` document or an accepted ADR, the repository version takes precedence. Conflicts must be reported and resolved explicitly rather than silently rewriting the accepted decision.

## Current documents

| Document | Purpose | Status |
| --- | --- | --- |
| [Project Charter](project/PROJECT_CHARTER.md) | Initial product purpose, boundaries, principles, and success direction | `DRAFT` |
| [Design Backlog](DESIGN_BACKLOG.md) | Ordered queue of documentation and design work | Living backlog |

## Planned documentation areas

- `project/` — project-level purpose, scope, and governance.
- `architecture/` — system architecture, domains, data, security, and performance.
- `adr/` — immutable records of significant architecture decisions.
- `standards/` — development and AI-assisted development standards.
- `specs/` — domain and feature specifications created when design work begins.

These directories are created only when they receive meaningful content. Empty placeholder documents and directories are intentionally avoided.

## Document lifecycle

Allowed statuses are:

- `PLANNED`
- `DRAFT`
- `REVIEW`
- `APPROVED`
- `DEPRECATED`
- `SUPERSEDED`

`APPROVED` records an accepted product or architecture decision. Its meaning must not be changed silently. A proposed change must identify the conflict, explain consequences, receive review, update affected documentation, and create a new ADR when the decision warrants one.

## Contribution workflow

For significant changes, use a branch and pull request:

1. Read the relevant current documentation.
2. Identify affected and dependent documents.
3. Make the smallest coherent change.
4. Update indexes or the design backlog when needed.
5. Review the diff before merge.

