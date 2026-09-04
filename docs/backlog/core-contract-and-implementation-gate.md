# Core contract and necessity gate

Status: Implemented

Created: 2026-09-05
Last updated: 2026-09-05
Prepared by: Codex
Implementation task: DFC-0002

## Resolution

The owner authorized implementation of the parts that pass the necessity gate.
The adopted contract lives in [the project brief](../PROJECT_BRIEF.md#core-contract)
and the rule in [the task workflow](../TASK_WORKFLOW.md#necessity-gate).
[ADR 0002](../adr/0002-core-contract-and-necessity-gate.md) records acceptance.
This record preserves provenance and review fixtures, not a second authority.

The contract, workflow, entry/contribution routing, task-template record and
bounded verification are necessary to make the requested rule usable. The
previously proposed separate pilot phase had no demonstrated necessity and was
excluded. Distribution packaging, long-term evidence work and automated semantic
checking were not activated.

## Discovery and evidence

The owner described implementations introducing complexity and prioritization
absent from intended behavior. That report motivated this proposal; source
code, runtime results and reported code reductions were not independently
verified here. Private source material is not reproduced.

Inspection found scope freeze but no explicit necessity argument against current
purpose in the workflow or task template. Whether the added gate reliably
prevents invented requirements in practice remains unmeasured; it inherits no
claim of baseline maturity.

The full original preparation is preserved in commit `f7ec301`. Adoption changes
are separately traceable and do not alter baseline provenance or the extraction
ledger. DFC-0001 remains the separate baseline-specification task.

## Synthetic acceptance fixtures

These cases specify expected review judgments. DFC-0002 records the actual
manual review and limitations. They are not runtime tests or proof that an
agent will follow the workflow. Keep the NG identifiers stable for citations.

| Case | Setup / proposed change | Expected result and evidence |
| --- | --- | --- |
| NG-01 | CC-03; fix a handoff template omitting skipped verification and next action | Pass in a scoped task; a completed sample contains both. |
| NG-02 | CC-03; build an automatic scheduler because it might help continuity | Fail: no required current outcome needs it; a runtime framework crosses the boundary. |
| NG-03 | Synthetic contract: return all matching records from three classes; add an early return after the first class | Fail: policy suppresses required results. A fixture matching all three must retain all three. |
| NG-04 | Synthetic contract: retain saved records; add a necessary schema migration | Pass within a migration charter with old-data upgrade and restart checks. |
| NG-05 | Synthetic contract: only owners may read private records; add an ownership check | Pass with a cross-owner read refusal check; "more secure" alone fails. |
| NG-06 | All fields are filled; CC-03 is cited with only "robustness" as necessity | Fail: no concrete consequence or distinguishing check. |
| NG-07 | A valid CC-04 index improvement is found in an unrelated frozen task | Route to backlog; contract relevance does not enlarge task scope. |
| NG-08 | Implementer broadens the contract to justify an unsupported fallback | Fail; propose a direction decision and hold dependent work. |
| NG-09 | Contract changes after Ready, invalidating planned behavior | Revalidate and pause or supersede as appropriate; the old revision cannot authorize invalid behavior. |
| NG-10 | Repair a contradictory sentence in an approved non-software brief-editing task | Pass with one grouped argument and before/after review; no per-line form or software build. |
| NG-11 | Bounded investigation compares two ways to preserve retrieval addresses under CC-04 | Pass with a question, bounded investigation and decision input; no implicit production implementation. |
| NG-12 | Gate fields pass but the diff adds an unrecorded second truth owner | Fail completion review; remove the addition or justify a canonical/derived relationship within authority and scope. |

NG-03 through NG-05 use invented product contracts; they impose no retrieval,
storage or security semantics on the protocol core.

## Handoff

The completed
[DFC-0002 record](../finished/DFC-0002_core-contract-and-necessity-gate.md)
contains adoption verification and limitations. The operating rule applies
through the normal task workflow; no separate pilot approval is required.
Future distribution needs its own explicit scope and publication approval under
the existing repository rules.
