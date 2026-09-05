# Current Task

Task ID: DFC-0001
Parent Task: None
Status: Draft
Owner: unassigned
Created: 2026-08-19
Last updated: 2026-09-05
Charter frozen at:

## Read First

- `AGENTS.md`
- `docs/TASK_WORKFLOW.md`
- `docs/PROJECT_BRIEF.md`
- `docs/CONTRIBUTING.md`
- `docs/CURRENT_STATUS.md`
- `docs/SYSTEMDOC.md`
- `docs/JOURNAL.md`
- `docs/FILESTRUCTURE.md`
- `baseline/README.md` and `extraction/ledger.md`

## Task Summary

Write `SPEC.md`: the normative requirements of the protocol, numbered so that
conformance results, issues and profiles can cite them precisely.

The material already exists. `baseline/acme-2026-08-19/` holds the hardened
model verbatim and `extraction/ledger.md` classifies twenty-eight rule groups as
CORE, PROFILE or PROJECT with an intended destination for each. This task turns
the CORE rows into requirements without softening them, and leaves the PROFILE
rows for the profile documents.

## Task Charter

The charter is editable while status is `Draft` and immutable once status is
`Ready`.

### Goal

Produce the normative specification of the protocol core, traceable rule by rule
to the baseline it came from.

### Primary Deliverable

`SPEC.md`, containing numbered requirements grouped by entry and ownership,
active work, continuity, containment, addressing, multiple actors and
resumability, together with the conformance levels that map onto them.

### In Scope

- Write one requirement per CORE row in `extraction/ledger.md`, keeping the
  force of the baseline rule and parameterizing only project identity.
- Group requirements and assign stable identifiers. An identifier, once written,
  is cited by conformance output and may not be renumbered.
- Define the conformance levels and state which requirements each level covers,
  and by what means each is checked: validator, git history, or a named review
  ritual.
- State, for every requirement, whether it is machine-checkable or ritual-checked.
  A requirement that is neither does not belong in the specification.
- Mark the four requirements whose baseline rules are hours old rather than
  months, so that a reader can weigh them accordingly.
- Update `extraction/ledger.md` so every CORE row names the requirement it
  became.
- Update `docs/CURRENT_STATUS.md` and `docs/FILESTRUCTURE.md`.

### Out of Scope

- Templates, profiles, the validator, examples, case studies, the evidence
  report. Each is its own task.
- Editing anything under `baseline/`.
- Choosing the final project name or changing the accepted Apache-2.0 license.
- Publishing a versioned protocol release.
- Simplifying or merging baseline rules. If a rule seems redundant, record the
  observation in `docs/backlog/` rather than dropping it; the model was hardened
  by failures that the text does not always show.

### Definition of Done

- Every CORE row in the ledger names the requirement it became, and every
  requirement names the ledger row it came from.
- Each requirement states its checking means.
- The conformance levels cover every requirement exactly once.
- The specification is readable in one sitting.
- `docs/CURRENT_STATUS.md` no longer says the specification does not exist.
- `docs/JOURNAL.md` has a signed entry and this task is archived.

### Necessity Gate

Contract: `docs/PROJECT_BRIEF.md`, Core Contract
Contract revision: `6bd0a8ae0787c441a87576403ce4ac264663580f`.

This Draft must be revalidated before Ready under `docs/TASK_WORKFLOW.md`.
The original baseline-transcription goals and boundaries are unchanged; this
section adds the operating requirement adopted in DFC-0002.

| Change | Clause and accepted constraint | Outcome; consequence if omitted | Smallest sufficient change | Planned check |
| --- | --- | --- | --- | --- |
| Transcribe the CORE ledger into the specification | CC-05; baseline provenance and the existing transcription charter | Make each requirement's origin and checking means inspectable; without the specification conformance cannot be evaluated | Numbered text and bidirectional ledger mapping, with no new rules presented as baseline extraction | Review ledger/specification mapping, checking means and conformance coverage |
| Record the verified result and handoff | CC-01, CC-03, CC-04 | Keep availability, location and remaining work accurate; otherwise a successor cannot distinguish delivered requirements from plans | Update the existing owning documents, journal and task archive | Reference/fence review, final diff review and named verification omissions |

### Minimum Verification Gates

- [ ] Every CORE ledger row maps to exactly one requirement, checked by reading
      the ledger end to end
- [ ] Every requirement maps back to a ledger row
- [ ] Manual link and fence review, since this repository has no tooling yet
- [ ] `git diff --check` clean

## References

- `baseline/acme-2026-08-19/AGENTS.md`
- `baseline/acme-2026-08-19/docs/TASK_WORKFLOW.md`
- `extraction/ledger.md`

## Checklist

- [x] Confirm DFC-0001 is claimed on `main` before freezing this charter
      (verified at `6b59508` on 2026-09-05; owner remains unassigned)
- [ ] Revalidate the Necessity Gate and resolve the recorded pre-freeze gaps
- [ ] Draft the requirement groups and identifiers
- [ ] Write one requirement per CORE ledger row
- [ ] Assign checking means to each requirement
- [ ] Define the conformance levels
- [ ] Mark the recently added requirements
- [ ] Backfill the ledger with requirement identifiers
- [ ] Update status and file structure
- [ ] Add a signed journal entry and archive this task

## Decisions and Notes

- DFC-0002 adopted the Core Contract and Necessity Gate under accepted ADR
  0002. Its completed record is
  `docs/finished/DFC-0002_core-contract-and-necessity-gate.md`. Apply the gate
  before this Draft becomes Ready. The new operating rule is not an extracted
  requirement and must not be inserted into the baseline ledger as one.
- Transcription, not redesign. A rewrite from memory keeps the parts that read
  well and drops the failure knowledge that is the actual value.
- Requirement identifiers are permanent. They will appear in conformance output,
  issue titles and profile documents, and those citations cannot be repaired
  afterwards.
- If a rule cannot be classified confidently as CORE, it is PROFILE. The core
  stays small; a profile rule can be promoted later, but a core rule that turns
  out to be local is expensive to remove.
- Repository publication and Apache-2.0 licensing were settled outside this
  task by the owner and are recorded in
  `docs/adr/0001-apache-2.0-open-source-distribution.md`. DFC-0001 neither
  chooses nor changes that boundary.

## Charter Amendment Log

Only non-semantic corrections are allowed after `Ready`.

-none

## Verification

- [ ] Ledger and specification cross-check, both directions
- [ ] Manual link and fence review
- [ ] `git diff --check`
- [ ] Document skipped checks and reasons

## Documentation Updates

- [ ] `docs/CURRENT_STATUS.md`
- [ ] `docs/FILESTRUCTURE.md`
- [ ] `docs/JOURNAL.md`
- [ ] `extraction/ledger.md`

## Handoff and Follow-ups

- Current state: Draft. The specification is unwritten. DFC-0002 is complete;
  the necessity gate applies to this task before its future freeze.
- Next recommended step: resolve the pre-freeze inconsistencies below and
  revalidate the gate, then draft requirement groups from the full CORE set.
- Blockers: the pre-freeze mapping and authority inconsistencies below.
- Child tasks: none.
- Follow-up: the completed DFC-0002 record contains adoption verification;
  no pilot prerequisite or additional adoption task remains.
- Resume condition: not applicable.
- Open questions: whether filenames are normative or only semantic roles are.
  The answer changes whether a renamed template breaks conformance, and it is
  listed as an open decision in `docs/PROJECT_BRIEF.md`.
- Pre-freeze reconciliation: the ledger has twenty CORE rows, including shared
  C-07 and C-18 destinations and a C-13/C-14 split, while this Draft charter
  requires one row per requirement. Resolve the mapping while the charter is
  editable. Also reconcile the open filename decision with the system document's
  assertion that roles are normative, and the identity register's allocation-only
  rule with its existing `Work` column. These are existing bootstrap gaps
  left with this Draft; they were outside DFC-0002.

## Finalize When Complete

- Archive this file under `docs/finished/`.
- Restore this template or populate the next approved task.
- Add a signed `docs/JOURNAL.md` entry.
- If Goal or Definition of Done changed, supersede this task instead of
  rewriting it.
