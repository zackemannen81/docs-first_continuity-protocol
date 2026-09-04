# Current Task

Task ID: DFC-0002
Parent Task: None
Status: Ready
Owner: Codex
Created: 2026-09-05
Last updated: 2026-09-05
Charter frozen at: 2026-09-05

## Read First

- `AGENTS.md`
- `docs/TASK_WORKFLOW.md`
- `docs/PROJECT_BRIEF.md`
- `docs/CONTRIBUTING.md`
- `docs/CURRENT_STATUS.md`
- `docs/SYSTEMDOC.md`
- `docs/JOURNAL.md`
- `docs/FILESTRUCTURE.md`
- `docs/adr/0002-core-contract-and-necessity-gate.md`
- `docs/backlog/core-contract-and-implementation-gate.md`

## Task Summary

Make the approved core contract and necessity gate operational in this
repository. The owner authorized implementation conditional on passing that
gate. Contract, workflow and template changes pass; a separate mandatory pilot
phase adds no necessary behavior and is excluded.

## Task Charter

The charter is editable while Draft and immutable once Ready.

### Goal

Require substantive changes here to demonstrate necessity for the approved
core contract as well as fit the frozen task charter.

### Primary Deliverable

The existing working documents with one authoritative core contract, a usable
necessity gate and verified examples of its application.

### In Scope

- Accept the owner-authorized direction in ADR 0002 and the project brief.
- Connect the entry point, workflow, contribution guidance and local task
  template to the contract and gate without duplicating their authority.
- Apply the gate to this adoption, review all twelve prepared scenarios and
  record actual reasoning and verification in this task.
- Resolve the preparation proposal at its existing path, update owning status,
  system, map and journal records, archive this task, and restore DFC-0001 as
  Draft with the gate required before its future freeze.

### Out of Scope

- A separate pilot phase, evidence collection programme or release prerequisite.
- Baseline or extraction-ledger changes, the full specification, distributed
  templates/profiles, validator/runtime code and automated semantic scoring.
- Unrelated bootstrap inconsistencies, mass refactoring or code removal.
- Pushes, remote identity publication, releases and announcements.

### Definition of Done

- The brief owns the approved contract and the workflow owns its gate.
- The entry point and contribution loop require the gate; the local template
  records authority, necessity, sufficient approach and verification.
- The gate covers pre-Ready review, material implementation changes, contract
  changes on resumption/integration and final review using existing routing.
- This task contains concrete gate arguments and results for all twelve cases,
  including rejection of invented policy and acceptance of necessary upkeep.
- A repository-only walkthrough can locate authority, consequences of failure,
  actual state, evidence and next work. Its self-review limitation is explicit.
- Owning documentation is current, this task is archived and DFC-0001 is
  restored as Draft without rewriting its baseline-transcription charter.

### Necessity Gate

Contract: `docs/PROJECT_BRIEF.md`, Core Contract
Contract revision: `6bd0a8ae0787c441a87576403ce4ac264663580f`.
Accepted constraint: ADR 0002 records the owner's instruction to implement
only changes that pass the necessity gate; no extra pilot prerequisite.

| Change | Clause and accepted constraint | Outcome; consequence if omitted | Smallest sufficient change | Planned check |
| --- | --- | --- | --- | --- |
| Establish the contract and decision | CC-01, CC-02; ADR 0002 | Find the approved purpose and require work to serve it; without an owner the gate has no authoritative referent | One short section in the existing brief and the existing ADR | Read clause references from this task and the entry point; confirm one owner |
| Require and record the gate | CC-02; ADR 0002 | Reject invented requirements even inside a task; without a procedure and record they can survive scope freeze | Add one workflow section, route to it from entry/contributing, add one template section | Twelve scenario verdicts and inspection of this completed gate |
| Verify and preserve continuity | CC-03, CC-04, CC-05 | A successor can tell what changed and what was checked; without this work proposal state and next task become misleading | Update existing records, resolve the existing proposal, archive and restore current task | Links/fences, historical-byte and charter checks, final diff review and handoff walkthrough |

### Minimum Verification Gates

- [ ] Review NG-01 through NG-12 against the adopted workflow with recorded verdicts.
- [ ] Verify contract discovery, template completeness and the final change set.
- [ ] Review live Markdown references/fences and collection discoverability.
- [ ] Confirm baseline, extraction, accepted ADR 0001, earlier journal entries
      and DFC-0001's original charter remain unchanged.
- [ ] Run `git diff --check` and check any new untracked file separately.

## References

- `docs/adr/0002-core-contract-and-necessity-gate.md`
- `docs/backlog/core-contract-and-implementation-gate.md` (preparation and fixtures)
- Preparation commit `f7ec301`; local-main identity claim `3c9fe46`.

## Checklist

- [x] Recheck main and archive; claim DFC-0002 on local main and integrate it.
- [x] Record the accepted contract and pin its committed revision before Ready.
- [ ] Freeze this bounded charter and implement the operating-document changes.
- [ ] Review scenarios, ownership, references and preserved history.
- [ ] Update durable records, archive DFC-0002 and restore DFC-0001 as Draft.

## Decisions and Notes

- Owner authority: on 2026-09-05 the owner instructed implementation if the
  proposed work passes the gate. The bounded adoption above passes; the
  previously suggested separate pilot stage has no demonstrated necessity.
- DFC-0001 is preserved on `codex/core-contract-preparation` at `f7ec301`.
  Restore its current-task file on completion. It was Draft, not a frozen
  blocked parent; this adoption neither supersedes nor implements it.
- The identity claim is committed on local main. Origin main was checked at
  `6b59508`; no remote claim was published. Reconcile the register with shared
  main before any future push; this local claim is not evidence of visibility
  or collision protection for remote collaborators.

## Charter Amendment Log

-none

## Verification

Pending execution. Synthetic review cases are semantic self-review, not
runtime tests or evidence of improved agent behavior.

## Documentation Updates

- [ ] `AGENTS.md`, `docs/PROJECT_BRIEF.md`, `docs/TASK_WORKFLOW.md`
- [ ] `docs/CONTRIBUTING.md`, `docs/template_CURRENT_TASK.md`
- [ ] `docs/adr/0002-core-contract-and-necessity-gate.md` and its index
- [ ] `docs/backlog/core-contract-and-implementation-gate.md` and its index
- [ ] `docs/CURRENT_STATUS.md`, `docs/SYSTEMDOC.md`, `docs/FILESTRUCTURE.md`
- [ ] `docs/JOURNAL.md`, finished-task collection, restored current task

## Handoff and Follow-ups

- Current state: Ready; contract accepted and pinned, identity on local main,
  DFC-0001 retained in the preparation commit.
- Next step: implement the gate in the existing working documents.
- Blockers: none for local adoption.
- Child tasks: none.
- Resume condition: not applicable.
- Deferred: baseline-specification inconsistencies stay with DFC-0001; remote
  identity reconciliation is required before any later publication.

## Finalize When Complete

- Archive this completed file as DFC-0002 in the finished-task collection.
- Restore DFC-0001 as Draft and add the newly required necessity gate.
- Add a signed journal entry recording actual checks and remaining limits.
