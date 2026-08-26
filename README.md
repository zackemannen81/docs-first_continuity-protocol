# docs-first continuity protocol

Open source and licensed under the Apache License 2.0.

This public repository is an extraction in progress and should be considered
a technical preview until a versioned release is published. Publication of the
source is not a protocol release or a conformance claim.

## The problem, in one story

A printer stops working and flashes red. A technician arrives and asks for the
manual and the service history.

Without docs-first, the answer is: "It might be in one of the twenty-five
binders on that shelf."

With docs-first, the answer is: "Start with the index in the yellow binder. It
points to the printer specification in the blue binder, page 99." Beside the
specification is a dated note: the same red light was a fuse, here is where the
fuse sits, here is how it was replaced, here is what was verified, and here is
who did it.

The technician does not read twenty-five binders and does not need to find the
person who did the last repair. The system routes one current problem to the
right specification, the relevant prior change and the next action.

Twenty-five binders are also documentation. They are not a knowledge system. The
difference is a known entry point, one owner per truth, a route to the
authority, and a dated record of what changed.

## What this repository is

An extraction in progress. The hardened working model lives frozen in
`baseline/`, `extraction/ledger.md` classifies each of its rules as core,
profile or project-specific, and `docs/` is this project running that model on
itself.

That last part is deliberate. A continuity protocol whose own repository cannot
be picked up by a stranger has answered its own question.

## What exists today

| | |
| --- | --- |
| Frozen baseline, verified against a tag | yes |
| Extraction ledger | yes |
| This repository's own docs-first instance | yes |
| Specification, templates, validator, profiles, evidence report | no |

`docs/CURRENT_STATUS.md` is the authority on that table. If they disagree, the
status document is right and this one is stale.

## Where to start reading

`AGENTS.md`, then the reading order it names. The active task is always
`docs/CURRENT_TASK.md`.

## License

This repository is licensed under the Apache License 2.0.

Using the Docs-First Continuity Protocol does not cause a project's own
documents, source code, or other artifacts to become licensed under
Apache-2.0.

Files copied or adapted from this repository remain subject to the terms
of the Apache License 2.0.
