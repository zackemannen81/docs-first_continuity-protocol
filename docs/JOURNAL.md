# Journal

Newest first. Append only: entries are never edited or reflowed, because other
records cite them and because their value is that they record what was believed
at the time.

## 2026-08-26 — Apache-2.0 open-source status reconciled

- Date: 2026-08-26
- Author: Codex
- Task: owner-directed truth repair. No DFC identity was allocated; DFC-0001
  remains the existing Draft specification task and neither chose nor changed
  this distribution boundary.
- Owner decision: the docs-first continuity protocol and its separately
  published multi-agent orchestrator add-on are open source under the Apache
  License 2.0.
- Change: `docs/adr/0001-apache-2.0-open-source-distribution.md` records the
  accepted boundary. The live entry point, guardrails, brief, status, system
  document, file map and DFC-0001 out-of-scope wording now agree that this is a
  public Apache-2.0 technical preview, not a versioned protocol release or a
  conformance claim. The add-on states the same license and explains that its
  npm `private` field prevents registry publication without making its source
  private. Its reviewed bootstrap example now selects `apache-2.0`.
- Historical record: the 2026-08-19 bootstrap entry remains unchanged. Its
  private/unlicensed statement records the earlier state and is superseded for
  current reality by this entry and the accepted decision.
- Verification: all 20 live protocol Markdown files and all 11 add-on
  Markdown files had resolving relative links and balanced code fences;
  `git diff --check` passed in both repositories; the add-on server built and
  passed 6/6 automated tests; and two clean bootstrap runs produced identical
  manifests with normalized `license_status=apache-2.0`.
- Not performed: no commit, push, release or announcement.
- Signature: Codex

## 2026-08-19 — Repository bootstrap from a frozen baseline

- Date: 2026-08-19
- Author: Claude
- Task: bootstrap, performed under `ACME-0173` in the source repository. This
  repository's own task numbering starts at DFC-0001, which is chartered but not
  started.
- Branch: `main`
- Change: this repository now exists as a docs-first instance running the model
  it intends to specify. `baseline/acme-2026-08-19/` holds fifteen files copied
  verbatim from tag `protocol-baseline-2026-08-19`
  (`75e4b5ee72201d02ad57f22b1a5fcfb3244d521e`) in `zackemannen81/acme-engine`,
  with provenance in `baseline/README.md`. `extraction/ledger.md` classifies
  twenty-eight rule groups as CORE, PROFILE or PROJECT.
- Verification: every copied file was compared by SHA-256 against
  `git show <tag>:<path>` at extraction. All fifteen matched. The comparison is
  repeatable against the tag, which is why the tag exists.
- Not copied, deliberately: the source repository's active charter, because it
  holds another contributor's in-progress work; `docs/JOURNAL.md`, because 6500
  lines of client, product and personal material must never be copied raw and
  journal evidence belongs to the evidence milestone, aggregated and anonymized;
  and the source project's status, architecture, brief and decisions, because
  the model is the workflow rather than the product it was used on.
- Identity prefix: `DFC`, encoding the descriptive method rather than a brand.
  The project name is undecided, and an identity carrying the name would need a
  rename that the addressing rule forbids.
- Honesty note: four rules in the baseline are hours old, not months.
  Path stability, collection discoverability, tense-aware citation validation
  and trunk identity claims were each added on 2026-08-19 after a real failure
  in the source repository. `extraction/ledger.md` marks them so that the
  evidence report does not treat them as equally proven.
- Handoff: DFC-0001 is chartered in `docs/CURRENT_TASK.md` as `Draft` and
  unassigned. It writes `SPEC.md` from the CORE rows of the ledger. Claim the
  identity on `main` before freezing it. This repository is private and
  unlicensed, and is therefore not open source.
- Signature: Claude
