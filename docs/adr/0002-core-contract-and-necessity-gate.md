# ADR 0002 — Core contract and necessity gate

Status: Proposed

Date: 2026-09-05
Prepared by: Codex
Decision owner: project owner; acceptance not recorded.

## Context

Scope freeze bounds implementation by a charter, but does not establish that
the charter or implementation is necessary for the current approved purpose.
The owner requested preparation of a first evolution addressing this gap.

The approved bootstrap direction is extraction by transcription. DFC-0001 must
preserve baseline provenance; a new rule needs an explicit decision and its own
evidence rather than being presented as an extracted rule.

## Proposed decision

Trial a **Core Contract** and **Necessity Gate** locally. The
[implementation proposal](../backlog/core-contract-and-implementation-gate.md)
contains adoption text, a candidate contract, template insertion and scenarios.

- Keep the short contract in the document owning approved direction: a section
  of this repository's project brief, not a second owner or a copy per task.
- Require an exact clause, observable outcome and consequence of omission,
  smallest sufficient approach, and verification. Frozen task scope must also
  permit the change.
- Missing necessity holds the affected change and invokes existing routing.
  Ordinary technical choices supported by those authorities need no new
  owner-approval ceremony.
- New requirements need an explicit direction decision. Engineering preference,
  existing code or filled fields cannot supply product authority.
- Store arguments in the task charter and results in Verification. Revalidate
  on material changes and review the actual diff before completion.
- Keep baseline extraction separate. Evaluate this new rule locally and later
  as an opt-in extension before considering core promotion or maturity claims.

## Alternatives considered

| Alternative | Assessment |
| --- | --- |
| Scope freeze alone | A frozen task can still contain an unnecessary requirement. |
| Advisory sentence in the entry point | Supplies no recorded necessity argument or review procedure. |
| Mandatory standalone product-contract file | Duplicates the existing direction owner here and assumes an undecided file-layout boundary. |
| Automated necessity score or code-size limit | Structural metrics cannot establish need; adds machinery before the practice has evidence. |
| Insert the rule directly in the baseline specification | Blurs provenance and generality; no extraction row supplies this rule. |

## Consequences

If accepted, update the brief, entry point, workflow and local task template in
one bounded adoption task. Review both rejection of invented needs and
acceptance of legitimate maintenance and non-software work. Record mistaken
rejections and administrative burden before claiming effectiveness.

This record is Proposed until explicitly accepted. It does not settle normative
filenames, change licensing, edit the baseline, activate implementation or
authorize external publication.
