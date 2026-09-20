# Decision Records

Discoverability: index. Every member of this directory is listed below.
Member state: required. Every member declares a `Status:` line under its title.

A decision record is written when a choice constrains future work: the shape of
the specification, compatibility, versioning, licensing mechanics, or anything
that would be expensive to reverse.

A record states the context, the decision, the alternatives considered and the
consequences. Superseded records stay, marked, with a link to what replaced
them. They are never deleted, because the reasoning is the point.

## Records

- `0001-apache-2.0-open-source-distribution.md` — accepted; public open-source
  distribution under Apache License 2.0, distinct from a versioned protocol
  release or conformance claim.
- [`0002-core-contract-and-necessity-gate.md`](0002-core-contract-and-necessity-gate.md)
  — accepted; adopt a core contract and necessity gate in the working documents,
  with separate provenance and no mandatory pilot phase.
- [`0003-atomic-semantic-ownership.md`](0003-atomic-semantic-ownership.md)
  — accepted; current owning state is truth for a semantic concern, with
  authorized ordered replacement and immutable historical provenance.

The remaining open decisions listed in `docs/PROJECT_BRIEF.md` each need their
own record when settled.
