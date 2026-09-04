# File Structure

The repository map. Update it in the same change as the structure it describes.

```text
docs-first_continuity-protocol/
├── AGENTS.md                       entry point and operating rules
├── README.md                       what this is, for a first-time reader
├── LICENSE                         Apache License 2.0 for this repository
├── docs/
│   ├── CURRENT_TASK.md             the active task, one per branch
│   ├── template_CURRENT_TASK.md    charter form with necessity arguments
│   ├── TASK_WORKFLOW.md            states, necessity gate, freeze, routing, identity
│   ├── PROJECT_BRIEF.md            core contract, direction and non-goals
│   ├── CONTRIBUTING.md             how work is done here
│   ├── CURRENT_STATUS.md           what exists now, and the gaps
│   ├── SYSTEMDOC.md                the durable shape of the protocol
│   ├── JOURNAL.md                  dated, signed work waves, append-only
│   ├── FILESTRUCTURE.md            this file
│   ├── TASK_IDS.md                 identity claims, allocation only
│   ├── adr/                        decisions
│   │   ├── README.md               decision index and status
│   │   ├── 0001-apache-2.0-open-source-distribution.md
│   │   └── 0002-core-contract-and-necessity-gate.md  accepted adoption
│   ├── backlog/                    non-activated proposals
│   │   ├── README.md               proposal index and status
│   │   └── core-contract-and-implementation-gate.md  provenance and review fixtures
│   ├── paused/                     frozen parents awaiting a condition
│   ├── finished/                   archived tasks, immutable
│   │   ├── README.md               archive naming convention
│   │   └── DFC-0002_core-contract-and-necessity-gate.md  completed adoption
│   └── concepts_sandbox/           excluded ideas, never authority
├── baseline/
│   ├── README.md                   provenance and what was not copied
│   └── acme-2026-08-19/            fifteen files, verbatim, never edited
└── extraction/
    └── ledger.md                   baseline rules classified CORE/PROFILE/PROJECT
```

## Conventions

Every collection under `docs/` declares one discoverability mode in its
`README.md`: `index`, meaning every member is listed there, or a naming
convention that makes every member addressable without a list. `docs/finished/`
uses the convention `DFC-NNNN_task-slug.md`; the others are indexed.

Collections whose members carry lifecycle state also declare
`Member state: required`, and each member declares a `Status:` line under its
title. State lives in content and in the index, never in a filename.

A record cited by `docs/JOURNAL.md`, `docs/finished/` or an accepted decision
keeps its path. Renaming it cannot be repaired, because the citations live in
records that may not be edited.

## Not yet present

The specification, templates, profiles, conformance validator, case studies and
evidence report do not exist. When they arrive they will sit beside `docs/` as
`SPEC.md`, `templates/`, `profiles/`, `conformance/`, `examples/` and
`case-studies/`, and this map must be updated in the same change.
