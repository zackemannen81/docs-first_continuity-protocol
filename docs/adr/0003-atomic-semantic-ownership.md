# ADR 0003 — Atomic semantic ownership and current-state precedence

Status: Accepted

Date: 2026-09-20
Prepared by: A008 operator
Decision owner: project owner

Approval: the owner direction recorded in DFC-0003 states that, for the same
semantic concern, current state is truth. This decision adopts that direction
as a protocol rule.

## Context

A repository may correctly preserve older ADRs, archived tasks and journal
entries while a later authorized task or decision changes what applies now. If
all records remain parallel authority, a successor must subjectively reconcile
historically valid but incompatible statements. Retrieval makes this failure
more likely: finding an older record does not make it current.

Deleting or rewriting old records would destroy provenance. A global version
registry, database or semantic-memory service would add mechanism outside the
protocol's scope.

## Decision

For each semantic concern, the current owning state is the truth. A semantic
concern is the smallest independently changeable boundary of a rule, outcome,
policy, decision or factual assertion.

- An authorized later task or decision that changes a concern atomically updates
  the current owning state/documentation in the same change.
- That state takes current ownership only of the boundary it changes. An earlier
  record is partially superseded when it retains unrelated boundaries whose
  current ownership has not changed.
- Earlier ADRs, finished tasks and journal entries remain immutable history and
  provenance. They explain how the current state was reached; they do not
  compete as current authority.
- Authorized order matters only after the semantic concern matches. A newer
  historical description does not take current ownership, and recency,
  retrieval or citation alone never makes a record authoritative.
- Resolve apparent contradiction by current owner, semantic concern and
  authorized order, rather than voting among retrieved documents.

`docs/PROJECT_BRIEF.md` owns the required CC-01 outcome;
`docs/TASK_WORKFLOW.md` owns the operating procedure; and
`docs/SYSTEMDOC.md` explains the durable model. The future DFC-0001
specification must transcribe this adopted rule as a new protocol requirement,
with provenance to this decision rather than to the frozen baseline.

## Alternatives considered

| Alternative | Assessment |
| --- | --- |
| Treat all historically valid records as concurrent authority | Leaves successors to subjectively reconcile conflicts and fails CC-01. |
| Rewrite or delete old records | Destroys inspectable provenance and violates immutable-history duties. |
| Use recency alone | A newer record can describe history or lack authority over the concern. |
| Add a global authority registry, graph engine or database | Adds runtime/storage machinery without a required outcome. |

## Consequences

Current owners must be updated in the same change as an authorized state change.
Historical records retain their paths and content. Documentation and future
specification work must distinguish historical correctness from current
authority, including partial supersession. No runtime, storage service or global
version scheme is introduced.
