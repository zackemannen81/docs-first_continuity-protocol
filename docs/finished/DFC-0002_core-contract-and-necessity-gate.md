# Current Task

Task ID: DFC-0002
Parent Task: None
Status: Complete
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

- [x] Review NG-01 through NG-12 against the adopted workflow with recorded verdicts.
- [x] Verify contract discovery, template completeness and the final change set.
- [x] Review live Markdown references/fences and collection discoverability.
- [x] Confirm baseline, extraction, accepted ADR 0001, earlier journal entries
      and DFC-0001's original charter remain unchanged.
- [x] Run `git diff --check` and check any new untracked file separately.

## References

- `docs/adr/0002-core-contract-and-necessity-gate.md`
- `docs/backlog/core-contract-and-implementation-gate.md` (preparation and fixtures)
- Preparation commit `f7ec301`; local-main identity claim `3c9fe46`.

## Checklist

- [x] Recheck main and archive; claim DFC-0002 on local main and integrate it.
- [x] Record the accepted contract and pin its committed revision before Ready.
- [x] Freeze this bounded charter and implement the operating-document changes.
- [x] Review scenarios, ownership, references and preserved history.
- [x] Update durable records, archive DFC-0002 and restore DFC-0001 as Draft.

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
- Implementation choice: retain the fixture IDs at the proposal's cited path,
  but replace its duplicated candidate contract and procedures with links to
  their adopted owners. Original preparation remains in commit `f7ec301`.
- Necessity self-check: the separate pilot stage, distribution packaging and
  semantic checker have no required outcome in this adoption charter. They
  were excluded; routine scenario review verifies the requested rule directly.

## Charter Amendment Log

-none

## Verification

### Scenario review — 2026-09-05, Codex

Manual semantic self-review of the twelve retained fixtures. Expected verdicts
agree with the adopted procedure in every case. This does not execute a product
or measure whether another actor will follow the rule. Existing guardrails
already covered some refusals; no claim that the new gate alone caused them.

| Case | Existing workflow coverage | Actual gate verdict and reason |
| --- | --- | --- |
| NG-01 | Handoff duties already require useful next steps and verification | Pass: CC-03 needs the omitted information; one template repair and an inspected sample suffice. |
| NG-02 | The brief already excludes runtime frameworks | Fail: a scheduler also lacks an omission consequence required by CC-03. The gate supplies an explicit necessity refusal, not a new framework prohibition. |
| NG-03 | Scope freeze alone does not compare an early return with product behavior | Fail: the supplied contract requires all three matching classes; the proposed early return excludes two. Retaining all three is the distinguishing check. |
| NG-04 | Task scope can authorize migration work but supplies no necessity argument | Pass: the assumed required migration protects the fixture's saved-record promise. Old-data upgrade plus restart verifies that promise, subject to the migration charter. |
| NG-05 | Safety duties may already require access control | Pass: the fixture's owner-only contract identifies a concrete unauthorized-read risk and cross-owner refusal check. A generic security label would fail. |
| NG-06 | A scope-compliant task may still use vague engineering language | Fail: CC-03 plus the word robustness names neither an omission consequence nor an observable check. Filled fields are explicitly insufficient. |
| NG-07 | Existing discovery routing already protects frozen scope | Backlog: a useful CC-04 change still fails the unrelated task's scope boundary. Both authorities are necessary. |
| NG-08 | Direction already needs explicit approval | Fail: implementation convenience cannot authorize a fallback or amend the contract. Existing owner authorization can be reused, but none covers this fixture's new behavior. |
| NG-09 | Freeze preserves the old agreement but does not explicitly revalidate it against changed purpose | Hold dependent work and revalidate; pause for a prerequisite or supersede an invalid charter. A pinned revision cannot override the current accepted boundary. |
| NG-10 | Documentation accuracy is already required | Pass: a grouped correction restores a named outcome using a before/after review. The gate requires no software build or per-line justification. |
| NG-11 | A bounded task can authorize an investigation | Pass: CC-04 supplies a concrete uncertainty and a decision-input deliverable. The explored production design remains unauthorized. |
| NG-12 | One owner per truth already rejects independent competing authorities | Fail completion: compare actual changes with the gate; reject a second owner. A justified derived view would need a canonical relationship and fit current scope. |

### Adoption self-check

The contract owner and accepted direction supply the first gate row. The
workflow, entry/contribution references and template implement the second.
Current records, fixture preservation and completion evidence implement the
third. No runtime, validator, extra collection or mandatory pilot was added.
NG-03 provides the requested refusal of invented priority; NG-04, NG-05 and
NG-10 preserve legitimate maintenance and documentation work.

### Documentation and handoff review

- Ad hoc checks passed for live Markdown links and anchors, balanced fences,
  indexed members and state, scenario fixture/result pairs and clause IDs.
- The frozen adoption charter matches commit `3b21113` except completed
  checkboxes. The contract and accepted ADR match `6bd0a8a`. The baseline,
  extraction and ADR 0001 are unchanged from `6b59508`; the earlier journal
  entries match `f7ec301` byte for byte after normalizing Git working-tree line
  endings. New-file whitespace is checked separately from tracked diff checks.
- Final change review maps every adoption surface to one of the three gate
  rows. The resolved proposal points to the current owners instead of retaining
  duplicate normative text. `git diff 6b59508 --check` passed.
- Repository-only handoff walkthrough: the entry point leads to the current
  task, the brief owns CC-01 through CC-05, and the workflow explains refusal
  and routing. Status distinguishes the adopted operating gate from the absent
  specification. This record contains the necessity arguments, twelve review
  results and omissions. DFC-0001 is the next Draft task; its pre-freeze gaps
  remain explicit. This is the implementing actor's self-review.
- Not performed: runtime tests (no runtime change), an independent newcomer
  test, long-term effectiveness measurement, baseline-source link repair,
  remote identity publication, push, release or announcement. No conformance
  badge or claim is made.

## Documentation Updates

- [x] `AGENTS.md`, `docs/PROJECT_BRIEF.md`, `docs/TASK_WORKFLOW.md`
- [x] `docs/CONTRIBUTING.md`, `docs/template_CURRENT_TASK.md`
- [x] `docs/adr/0002-core-contract-and-necessity-gate.md` and its index
- [x] `docs/backlog/core-contract-and-implementation-gate.md` and its index
- [x] `docs/CURRENT_STATUS.md`, `docs/SYSTEMDOC.md`, `docs/FILESTRUCTURE.md`
- [x] `docs/JOURNAL.md`, finished-task collection, restored current task

## Handoff and Follow-ups

- Current state: adoption and bounded verification complete.
- Next step: resume DFC-0001 from its restored Draft, resolving its existing
  pre-freeze gaps before freezing the baseline-specification charter.
- Blockers: none for local adoption.
- Child tasks: none.
- Resume condition: not applicable.
- Deferred: baseline-specification inconsistencies stay with DFC-0001; remote
  identity reconciliation is required before any later publication.

## Finalize When Complete

- Archive this completed file as DFC-0002 in the finished-task collection.
- Restore DFC-0001 as Draft and add the newly required necessity gate.
- Add a signed journal entry recording actual checks and remaining limits.
