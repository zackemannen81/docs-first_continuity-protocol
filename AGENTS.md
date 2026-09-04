# AGENTS.md

This repository is docs-first. Every task begins in `docs/CURRENT_TASK.md`.

It is also the specification of the method it uses. That is deliberate: a
continuity protocol whose own repository cannot be picked up by a stranger has
answered its own question.

## Project Identity

- Working project name: docs-first continuity protocol
- Repository: `docs-first_continuity-protocol`
- Task identity prefix: `DFC`
- Purpose: extract the hardened docs-first working model into an
  agent-neutral, domain-neutral protocol with a specification, templates and a
  conformance suite.
- Current phase: bootstrap. The frozen baseline and the extraction ledger
  exist. The specification, templates, profiles and validator do not.
- Status: public open-source technical preview, licensed under the Apache
  License 2.0. Public availability does not imply a versioned protocol release
  or a conformance claim.

## Start Here

Read these in order before changing the repository:

1. `docs/CURRENT_TASK.md`
2. `docs/TASK_WORKFLOW.md`
3. `docs/PROJECT_BRIEF.md`
4. `docs/CONTRIBUTING.md`
5. `docs/CURRENT_STATUS.md`
6. `docs/SYSTEMDOC.md`
7. `docs/JOURNAL.md`
8. `docs/FILESTRUCTURE.md`

Read decision records under `docs/adr/` when the task touches a decided
boundary.

## Documentation Ownership

- `docs/CURRENT_TASK.md`: the active task. One per branch.
- `docs/TASK_WORKFLOW.md`: task states, scope freeze, routing, identity.
- `docs/PROJECT_BRIEF.md`: approved direction, core contract and fixed scope.
- `docs/CURRENT_STATUS.md`: what exists now and what does not.
- `docs/SYSTEMDOC.md`: the durable shape of the protocol and this repository.
- `docs/JOURNAL.md`: dated, signed work waves. Append-only.
- `docs/FILESTRUCTURE.md`: repository map.
- `docs/TASK_IDS.md`: identity claims. Allocation only, never status.
- `docs/adr/`: decisions, alternatives and consequences.
- `docs/finished/`: archived completed tasks, immutable.
- `docs/paused/`: frozen parent tasks awaiting a resume condition.
- `docs/backlog/`: non-activated proposals.
- `docs/concepts_sandbox/`: excluded concept work. No task may cite it as
  authority.
- `baseline/`: the frozen source model. Provenance, never edited, never
  authority.
- `extraction/`: the classification of baseline rules into this project's own.

## Task Workflow

### Start

- Claim the identity in `docs/TASK_IDS.md` and merge that claim to `main`
  before moving the charter to `Ready`. The next free identity is one above the
  highest of the register and `docs/finished/`. A local count cannot see
  somebody else's branch.
- Fill `docs/CURRENT_TASK.md` from `docs/template_CURRENT_TASK.md` with goal,
  deliverable, scope, out-of-scope, definition of done and verification gates.
- Freeze the charter when status changes from `Draft` to `Ready`.

### Necessity gate

Before Ready and before substantive implementation, apply the Necessity Gate in
`docs/TASK_WORKFLOW.md` against the Core Contract in `docs/PROJECT_BRIEF.md`.
Record the exact clause, observable necessity, smallest sufficient change and
verification in the task. A change must pass this gate and fit the frozen
charter. Missing necessity means do not implement the affected change; use the
existing routing rules. Recheck material changes and the final diff as the
workflow requires.

### During work

- Work from the checklist and keep it truthful.
- Do not expand or redefine a frozen goal, deliverable, scope or definition of
  done.
- Route every discovery: inside the charter it becomes a checklist item; if it
  blocks, pause the parent and activate a bounded child; if it is in project
  scope but not needed now, it goes to the backlog; if it is outside project
  scope, it goes to the concepts sandbox.
- Update durable documentation in the same change as what it describes.

### Pause or handoff

- Record blockers, next steps, verification gaps and a resume condition.
- Add a dated, signed entry to `docs/JOURNAL.md`.
- The next actor must be able to resume from the repository alone.

### Finish

- Verify in proportion to risk and state what was not verified.
- Archive the task under `docs/finished/` as `DFC-NNNN_task-slug.md`.
- Restore `docs/CURRENT_TASK.md` from the template, or fill it with the next
  approved task.

## One Active Task, Per Branch

- At most one task is active per branch, held in that branch's
  `docs/CURRENT_TASK.md`. Version control already provides exactly one copy per
  branch, so this states the rule where it is already enforced.
- The trunk never states how many tasks are active anywhere.
  `docs/TASK_IDS.md` records that an identity is taken, which says nothing
  about activity.
- A branch merges when its task is complete, so `main` normally carries the
  restored template. A merged in-progress charter is an explicit exception.

## Addressing and Discoverability

- A record's path is its identity. Status is declared in the record's content
  and in its collection index, never in a filename or a location.
- A file cited by append-only or archived documentation keeps its path, whatever
  its type. Renaming it is not repairable: fixing the citations would mean
  editing records that must not be edited.
- Do not cite disposable material from an immutable record. Give it a stable
  path first, or describe it instead of linking it.
- Every collection declares one discoverability mode in its `README.md`:
  `index`, meaning every member is listed there, or a naming convention that
  makes every member addressable without a list.

## Evidence Discipline

This project's central claim is that its model has been used, not that it
sounds reasonable. That obligation applies to the repository itself.

- Do not state that something is tested, proven or adopted without naming the
  evidence.
- Distinguish observed facts, supported inferences and open hypotheses.
- Private material from the source projects is never published raw. Aggregate,
  anonymize, and obtain consent for excerpts.
- Rules added recently carry less evidential weight than rules in continuous
  use for months. `extraction/ledger.md` records which is which.

## Safety

- Never commit credentials, personal data or client material.
- The repository is public and licensed under Apache-2.0. Private source
  material, credentials and personal data remain prohibited.
- New releases, announcements and other external effects require explicit
  approval.
