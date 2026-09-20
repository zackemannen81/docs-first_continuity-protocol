# Current Task

Task ID: DFC-0003
Parent Task: None
Status: Ready
Owner: A008 operator
Created: 2026-09-20
Last updated: 2026-09-20
Charter frozen at: 2026-09-20

## Read First

- `AGENTS.md`
- `docs/TASK_WORKFLOW.md`
- `docs/PROJECT_BRIEF.md`
- `docs/CONTRIBUTING.md`
- `docs/CURRENT_STATUS.md`
- `docs/SYSTEMDOC.md`
- `docs/JOURNAL.md`
- `docs/FILESTRUCTURE.md`
- Relevant records under `docs/adr/`
- The pre-existing DFC-0001 Draft on `main`; this task must not erase or redefine that separate specification task.

## Task Summary

Make authority in docs-first follow the same atomic ownership rule as durable state: for a given semantic concern, **the current owning state is the truth**. When a later authorized task or decision changes that same concern, the later state atomically takes ownership and the previous state becomes history/provenance.

Older ADRs, finished tasks and journal records remain immutable evidence of what previously applied. They must not continue to compete as parallel current authority after a later authorized decision has replaced the same semantic state.
## Task Charter

### Goal

Define and adopt atomic semantic ownership and current-state precedence as a core continuity rule, so a competent successor can answer “what applies now?” without reconciling a pile of historically valid but mutually incompatible records.

### Primary Deliverable

An accepted protocol decision plus the smallest changes to the Core Contract, task workflow and owning documentation needed to establish:

1. one current owner/state per semantic concern;
2. later authorized state on the same concern takes ownership;
3. prior state remains immutable history/provenance;
4. partial replacement affects only the semantic boundary actually changed;
5. time/order is part of authority resolution;
6. historical records never regain current authority merely because retrieval finds them.

### In Scope

- Record the 2026-09-20 owner direction as an explicit protocol decision.
- Refine the Core Contract, primarily the “find the authority” outcome, so current authority and historical authority cannot be confused.
- Define a semantic concern/address narrowly enough that two unrelated decisions may coexist while two sequential decisions about the same concern cannot both be current.
- Require an authorized later task/decision changing the same concern to atomically update the current owning state/documentation in the same change.
- Preserve the prior ADR/task/journal record unchanged as history/provenance.
- Define partial supersession: a later decision may take ownership of one clause/boundary without falsely invalidating unrelated parts of the older record.
- Make temporal/order semantics explicit: later authorized state wins for the same concern unless the later record explicitly describes historical state rather than changing current state.
- Update protocol guidance so agents resolve current truth from the current owner first and use historical records to explain how that state was reached.
- Feed the adopted rule into the still-Draft DFC-0001 specification task without silently rewriting that task’s goal.
### Out of Scope

- A runtime service, database, graph engine or semantic-memory implementation.
- A global hash/version scheme for documents.
- Requiring every historical ADR to be rewritten.
- Deleting or mutating immutable finished tasks, ADR history or journal entries.
- Treating recency alone as authority when a later record is not authorized to own the concern.
- Making every document a competing source that must be re-reconciled on each read.
- Renaming stable cited files.
- Solving unrelated open decisions such as final project name or normative filenames.
- Expanding DFC-0001 beyond incorporating the adopted ownership rule into its future specification work.

### Definition of Done

- The protocol states plainly that current owning state is the truth for a semantic concern.
- A later authorized decision changing the same concern replaces the previous current state atomically; the previous value remains historical provenance.
- An older ADR cannot override a later authorized task/decision merely because both are retrieved or cited.
- Partial supersession is representable without declaring an entire older record invalid.
- The protocol distinguishes “historically correct” from “currently authoritative”.
- A newcomer can resolve a two-record contradiction by ownership + semantic address + order, without subjective document voting.
- The rule is reflected in Core Contract/workflow/system documentation and queued for DFC-0001 specification transcription.
- No new runtime/storage mechanism is introduced.
### Necessity Gate

Contract: `docs/PROJECT_BRIEF.md`, Core Contract
Contract revision: `6bd0a8ae0787c441a87576403ce4ac264663580f`

| Change | Clause and accepted constraint | Outcome; consequence if omitted | Smallest sufficient change | Planned check |
| --- | --- | --- | --- | --- |
| Adopt current-state authority precedence | CC-01 — Find the authority; owner direction 2026-09-20 | A newcomer can otherwise find several historically valid contradictory records and still not know what applies now | Add one explicit semantic ownership/precedence rule and update current owning docs in the same change | Scenario review with older ADR + later authorized task changing the same concern |
| Preserve immutable history without parallel authority | CC-03 and CC-05 — usable handoff and inspectable claims | Deleting old decisions destroys provenance, while treating them as still-current makes the repository ambiguous | Keep historical records immutable; mark current ownership in current state/decision surfaces and explicit replacement links/wording only where needed | Review partial replacement and historical traceability scenarios |
| Keep the rule bounded and non-runtime | Core Contract: agent-neutral/domain-neutral continuity protocol; non-goal of runtime framework | An implementation-heavy authority graph would recreate the complexity this rule is intended to remove | Documentation/specification semantics only; no database/service/version engine | Final diff review for absence of runtime/storage mechanisms |

### Minimum Verification Gates

- [ ] Scenario: ADR A says X; later authorized task/decision says Y for the same concern; current authority resolves to Y and X remains historical.
- [ ] Scenario: later decision changes only one clause of an older ADR; unrelated clauses retain their current ownership.
- [ ] Scenario: two records about different semantic concerns coexist without false supersession.
- [ ] Scenario: a historical description written later does not become current merely because its file/commit is newer.
- [ ] Scenario: a stale retrieved ADR cannot override the current owner.
- [ ] Review DFC-0001 Draft impact and record exactly how the new rule enters its future specification work without redefining that task.
- [ ] Manual link/fence review and `git diff --check`.
- [ ] Final Necessity Gate review against actual diff.
## References

- `docs/PROJECT_BRIEF.md` CC-01, CC-03, CC-05
- `docs/TASK_WORKFLOW.md`
- `docs/SYSTEMDOC.md`
- `docs/adr/README.md`
- `docs/finished/DFC-0002_core-contract-and-necessity-gate.md`
- DFC-0001 Draft on `main`
- Owner direction recorded 2026-09-20 in this charter.
- A008-0143 is an implementation-specific sibling task and is not protocol authority; this DFC task generalizes only the continuity/ownership principle.

## Checklist

- [ ] Re-read current authority rules and identify every place where old and new decisions can appear to remain concurrently authoritative.
- [ ] Write failing/resolution scenarios before changing protocol text.
- [ ] Record the explicit decision adopting atomic semantic ownership/current-state precedence.
- [ ] Update Core Contract and workflow with the smallest sufficient wording.
- [ ] Update SYSTEMDOC/CURRENT_STATUS as observed protocol state changes.
- [ ] Define partial supersession and historical provenance without inventing a new registry/database.
- [ ] Record how DFC-0001 Draft must consume the adopted rule when specification work resumes.
- [ ] Run scenario review, link/fence review and `git diff --check`.
- [ ] Review final diff against scope and remove/reroute unrelated architecture.
- [ ] Archive/handoff and restore the pre-existing DFC-0001 Draft as the branch’s next current task before integration.

## Decisions and Notes

- Owner decision, 2026-09-20: **state = truth**. For the same semantic concern, a later authorized update takes current ownership atomically; the previous state becomes history.
- “Later” alone is not enough. The later record must be authorized to own/change that semantic concern.
- History is not wrong merely because it is no longer current.
- ADRs are historical decision records, not immortal parallel truth. A later authorized task/decision can take ownership of the same boundary.
- Partial replacement is preferred over pretending an entire older ADR is invalid when only one decision changed.
- Current-state lookup must not require subjective voting across all retrieved documentation.
- Keep this rule simple: semantic address/concern + current owner/state + ordered history/provenance.
- Git/HEAD analogy: with one `main`, a change starts from current HEAD, changes only the affected files, and commits a new HEAD. The new HEAD is current truth; prior commits remain immutable history. Docs-first authority must work the same way per semantic concern: later authorized state becomes current ownership, while older decisions remain provenance rather than parallel current truth.
## Charter Amendment Log

- none

## Verification

- [ ] Record scenario-review results.
- [ ] Record exact documents/clauses updated.
- [ ] Record `git diff --check`.
- [ ] Record any skipped checks and reasons.

## Documentation Updates

- [ ] `docs/PROJECT_BRIEF.md`
- [ ] `docs/TASK_WORKFLOW.md`
- [ ] `docs/SYSTEMDOC.md`
- [ ] `docs/CURRENT_STATUS.md`
- [ ] relevant ADR/index documentation
- [ ] DFC-0001 Draft follow-through note/inputs, without changing its frozen state because it remains Draft
- [ ] `docs/JOURNAL.md`
- [ ] `docs/FILESTRUCTURE.md` only if structure changes

## Handoff and Follow-ups

- Current state: Ready on dedicated DFC-0003 branch.
- Next recommended step: implement the decision/document changes before DFC-0001 is frozen, then restore DFC-0001 as current Draft for specification work.
- Blockers: DFC-0002 completed branch is the current governance baseline; integrate in normal operator order before final DFC-0003 integration if main has not yet received it.
- Child tasks: none at freeze.
- Resume condition: revalidate against the current Core Contract if DFC-0002 or DFC-0001 changes materially first.
- Open questions: exact wording/placement of partial supersession metadata may be refined within this charter, but no new authority registry or runtime may be introduced.

## Finalize When Complete

- Archive as `docs/finished/DFC-0003_atomic-authority-ownership.md`.
- Restore the pre-existing DFC-0001 Draft as `docs/CURRENT_TASK.md` before final integration.
- Add signed `docs/JOURNAL.md` entry.
- Push/open PR; do not merge from a worker.
