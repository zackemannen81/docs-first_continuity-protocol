# Current Status

Reality as of 2026-09-05. This document describes what exists, not what is
planned. If it disagrees with the code or the tree, this document is wrong and
must be corrected.

## What exists

| Thing | State |
| --- | --- |
| `baseline/acme-2026-08-19/` | Fifteen files, copied verbatim from tag `protocol-baseline-2026-08-19` in the source repository, verified byte for byte at extraction |
| `baseline/README.md` | Provenance: source repository, revision, date, extractor, and what was deliberately not copied |
| `extraction/ledger.md` | Twenty-eight classified rule groups, plus four rules marked as added hours before extraction |
| This repository's own docs-first instance | Complete and operating: entry point, active task, workflow, brief, status, system document, journal, file map, identity register, collection indexes |
| `LICENSE` and public source repository | Open source under the Apache License 2.0; publication is a technical preview, not a versioned protocol release or conformance claim |
| `docs/backlog/core-contract-and-implementation-gate.md` and proposed ADR 0002 | Definition, candidate contract, gate text, twelve synthetic acceptance cases and adoption plan; the gate has not been adopted |

## What does not exist

The following deliverables or capabilities are not available.

- The specification. No requirement is normative yet; `extraction/ledger.md`
  names intended destinations such as C-01, but those requirements are not
  written.
- The templates, in any profile.
- The conformance validator. This repository is checked by reading it.
- The profiles: software, creative production, operations, research.
- The case studies and the evidence report.
- An adopted core contract or necessity gate. The proposal is preparation,
  not a change to the current workflow or a released extension.
- A final name decision or a versioned protocol release.

## Known gaps and risks

- **The specification does not exist, so conformance cannot be claimed.** This
  repository follows the baseline model; it does not yet conform to a written
  standard, because there is none.
- **Public open source is not the same as a protocol release.** Apache-2.0 and
  public availability are settled, while the normative specification,
  templates, profiles and conformance suite remain absent.
- **Four rules in the baseline are hours old.** Path stability, collection
  discoverability, tense-aware citation validation and trunk identity claims
  were added on 2026-08-19 in response to real failures, and have not been used
  long enough to be called hardened. `extraction/ledger.md` marks them.
- **No tooling.** There is no link checker, no fence checker and no conformance
  validator here. Verification is manual review until the validator exists.
- **Evidence is not yet publishable.** The counting method has not been
  written, no consent has been obtained for excerpts, and no journal material
  has been anonymized.
- **Twenty-two links inside `baseline/` do not resolve**, because the baseline
  is a partial verbatim copy whose links point into the source repository. This
  is correct and must not be repaired. Any future link checker excludes
  `baseline/`.
- **The name is undecided**, which is why the task identity prefix `DFC`
  encodes the descriptive method rather than a brand. Identities cannot be
  renamed once cited.

## Boundaries that hold

- `baseline/` is never edited. Corrections belong in this project's documents.
- The source repository does not depend on this one. The relation is one way.
- This repository is public open source under the Apache License 2.0. That
  distribution decision does not license downstream projects that merely use
  the protocol and does not imply conformance or a versioned release.
