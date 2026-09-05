# ADR 0002 — Core contract and necessity gate

Status: Accepted

Date: 2026-09-05
Prepared by: Codex
Decision owner: project owner

Approval: on 2026-09-05 the owner instructed implementation if the proposed
work would pass the necessity gate. The contract, operating rule, template and
bounded verification meet that condition. A separate pilot phase does not
establish a necessary outcome and is excluded from this decision.

## Context

Scope freeze bounds implementation by a charter, but does not establish that
the charter or implementation is necessary for the current approved purpose.
The owner requested preparation of a first evolution addressing this gap.

The approved bootstrap direction is extraction by transcription. DFC-0001 must
preserve baseline provenance; a new rule needs an explicit decision and its own
evidence rather than being presented as an extracted rule.

## Decision

Adopt a **Core Contract** and **Necessity Gate** in this repository's working
documents. The
[implementation proposal](../backlog/core-contract-and-implementation-gate.md)
records preparation and scenario fixtures. The brief owns the adopted contract;
the workflow owns the gate. The proposal is not a second authority.

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
- Keep baseline extraction separate. This is a new operating rule with bounded
  verification, not evidence of long-term effectiveness. Adoption is effective
  when the working documents are updated; no separate pilot or evidence
  programme is required before it applies.

## Alternatives considered

| Alternative | Assessment |
| --- | --- |
| Scope freeze alone | A frozen task can still contain an unnecessary requirement. |
| Advisory sentence in the entry point | Supplies no recorded necessity argument or review procedure. |
| Mandatory standalone product-contract file | Duplicates the existing direction owner here and assumes an undecided file-layout boundary. |
| Automated necessity score or code-size limit | Structural metrics cannot establish need; adds machinery before the practice has evidence. |
| Insert the rule directly in the baseline specification | Blurs provenance and generality; no extraction row supplies this rule. |

## Consequences

Update the brief, entry point, workflow and local task template in DFC-0002.
Review both rejection of invented needs and acceptance of legitimate maintenance
and non-software work. Record actual checks and omissions without claiming
effectiveness beyond the evidence. Existing safety and external-effect rules
continue to apply.

This decision does not settle normative filenames, change licensing, edit the
baseline, specify distribution packaging or authorize external publication.
