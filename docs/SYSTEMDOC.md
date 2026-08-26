# System Document

The durable shape of the protocol and of this repository. Behaviour that is
implemented is described here; intentions belong in `docs/PROJECT_BRIEF.md`.

## The model in one page

```text
private actor context
  → explicit repository state
  → one bounded active task
  → only the authority that task names
  → work and verification
  → durable status, decision and handoff
  → next actor resumes without the previous actor's memory
```

The benefit is not documentation volume. It is work continuity with bounded
context loading: the reader loads the active task and the authority it names,
not the project's whole history.

## Semantic roles

The protocol is defined by roles, not filenames. A profile may rename the
presentation-facing documents, but it must preserve these roles or publish an
exact mapping.

| Role | This repository | Owns |
| --- | --- | --- |
| Entry and guardrails | `AGENTS.md` | Reading order, safety, operating rules |
| Active work | `docs/CURRENT_TASK.md` | One task's frozen charter, progress, verification, handoff |
| Task state machine | `docs/TASK_WORKFLOW.md` | States, freeze, routing, identity |
| Approved direction | `docs/PROJECT_BRIEF.md` | Purpose, goals, non-goals |
| Current reality | `docs/CURRENT_STATUS.md` | What exists now, and the gaps |
| Durable system model | `docs/SYSTEMDOC.md` | This document |
| Work history | `docs/JOURNAL.md` | Dated, signed evidence of work waves |
| Repository map | `docs/FILESTRUCTURE.md` | Where things live and why |
| Identity allocation | `docs/TASK_IDS.md` | Which identities are taken |
| Durable decisions | `docs/adr/` | Decisions, alternatives, consequences |
| Completed work | `docs/finished/` | Immutable archived tasks |
| Blocked work | `docs/paused/` | Frozen parents awaiting a condition |
| Future work | `docs/backlog/` | Non-activated proposals |
| Excluded ideas | `docs/concepts_sandbox/` | Undecided concepts, never authority |

## Why the sandbox exists

An idea has three possible destinations: an authoritative document, where it
contaminates the truth surface; a chat log, where it leaves the repository; or a
marked non-authority area. Only the third keeps both properties the protocol
depends on — nothing valuable leaves, nothing undecided gains authority.

The boundary is asymmetric. Material enters freely, with no identity, no charter
and no verification. It leaves only by being restated in an owning document
through an activated task or a decision record. Nothing becomes true by sitting
there, and nothing becomes true by being linked from an authoritative document.

The sandbox is also what makes the strict core survivable. Every rule that
freezes a charter or blocks scope growth creates pressure, and pressure with no
outlet is released by breaking the rule.

## Addressing

A record's path is its identity. Status lives in the record's content and in its
collection index.

This is structural rather than stylistic. Journal entries are append-only and
archived tasks are immutable, and they cite other records by path. Renaming a
cited record leaves two exits, and the protocol forbids one of them:

```text
rename a cited record
  → repair the citations       → requires editing append-only history: forbidden
  → leave the citations broken → the repository fails its own retrieval promise
  → restore the original path  → the only permitted exit
```

Validation of cited paths must distinguish tense. A document describing the
present must name paths that exist. The archive names files after they are gone
and the active charter names its deliverables before they exist; both
legitimately cite paths that do not resolve, and both should report without
gating.

## Identity allocation

Identities are claimed on the trunk before a charter freezes, in a strictly
ascending append-only register. The design goal is not exclusion, which is
unavailable between actors who cannot see each other's branches. It is a
guaranteed collision at a known point: two simultaneous claims edit the same
region and the second is a merge conflict.

The register records identity, never activity. A trunk-level statement about how
much work is in progress would contradict the one-active-task rule, which is
scoped per branch because that is where version control already enforces it.

## This repository's own structure

```text
docs-first_continuity-protocol/
├── AGENTS.md              entry point
├── README.md              public technical-preview entry point
├── LICENSE                Apache License 2.0
├── docs/                  this repository's own docs-first instance
├── baseline/              frozen source model, never edited, never authority
└── extraction/            classification of baseline rules into this project's
```

Three levels coexist and must not be confused:

| Level | Meaning |
| --- | --- |
| `docs/` | This project's live working state. It must pass whatever conformance the specification eventually defines. |
| `baseline/` | Provenance. Frozen, unedited, not authority for anything here. |
| `extraction/` | The audit trail between the two. |

Once templates exist they will form a fourth level: shipped artefacts carrying
placeholders, validated in template mode rather than as live state.
