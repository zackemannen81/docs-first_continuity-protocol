# ADR 0001 — Apache-2.0 open-source distribution

Status: Accepted

Date: 2026-08-26

Decision owner: Rickard Zakrisson

## Context

The repository received the standard Apache License 2.0 text and licensing
language in `README.md` and `docs/CONTRIBUTING.md`, but the live guardrails,
project brief and current-status documents still described the repository as
private, unlicensed and not open source. The repository therefore contradicted
itself about a basic distribution boundary.

The normative specification, templates, profiles and conformance suite do not
yet exist. Source availability and licensing must not be confused with a
versioned protocol release or a conformance claim.

## Decision

The docs-first continuity protocol repository is public open source under the
Apache License 2.0.

- `LICENSE` is the authoritative license text for repository contents unless a
  file states otherwise.
- Contributions intentionally submitted for inclusion use Apache-2.0 under
  `docs/CONTRIBUTING.md`.
- Merely using the protocol does not impose Apache-2.0 on a user's project,
  documents, source code or other artifacts.
- Public repository availability is a technical preview. A versioned protocol
  release requires a separate explicit decision and verified release work.
- Open-source publication does not claim conformance while the normative
  specification and conformance suite are absent.

## Alternatives considered

### Keep the repository private or all-rights-reserved

Rejected. It contradicts the owner's intended distribution and the license
already committed to the repository.

### Publish source without an open-source license

Rejected. Public visibility alone grants no clear reuse rights and would make
describing the project as open source inaccurate.

### Treat public availability as the first protocol release

Rejected. The repository truthfully states that the specification, templates,
profiles and conformance suite do not exist yet.

## Consequences

- All live repository documents must describe Apache-2.0 and public
  open-source status consistently.
- Historical journal entries and the frozen baseline remain unchanged; they
  record what was true or believed at their own revision.
- Release numbering, release artifacts and conformance remain future work and
  require explicit authority.
