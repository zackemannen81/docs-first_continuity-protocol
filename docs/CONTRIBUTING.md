# Contributing

## Licensing of contributions

Unless explicitly stated otherwise, contributions intentionally submitted
for inclusion in this repository are licensed under the Apache License 2.0.

## Required reading

`AGENTS.md` first, then the reading order it names. Do not start work from an
issue title alone.

## The loop

1. Claim an identity in `docs/TASK_IDS.md` and merge the claim to `main`.
2. Fill `docs/CURRENT_TASK.md` from the template.
3. Apply the Necessity Gate in `docs/TASK_WORKFLOW.md` to the Core Contract
   in `docs/PROJECT_BRIEF.md`, then move the task to `Ready` to freeze it.
4. Work the checklist, keeping it truthful as you go.
5. Review actual changes against the gate and charter, verify in proportion to
   risk, and state what you did not verify.
6. Update every affected owning document in the same change.
7. Archive the task and add a signed journal entry.

## Scope freeze

Once a charter is `Ready`, its goal, primary deliverable, scope, out-of-scope,
definition of done and minimum verification gates do not change. Gates may be
strengthened, never removed.

If the work turns out to need something outside the charter, route it: checklist
step, paused parent with a bounded child, backlog proposal, or concepts sandbox.
Doing it anyway is the failure this rule exists to prevent.

## Files cited by documentation

- Do not rename, move or delete a file that documentation cites. Citations from
  `docs/JOURNAL.md`, `docs/finished/` and accepted decisions cannot be repaired
  afterwards, because those records may not be edited.
- This binds every file type, not only Markdown.
- Do not cite disposable material from an immutable record. Give it a stable
  path first, or describe it instead of linking it. A directory called `temp`
  stops being temporary the moment an archived task names a file inside it.
- Express state in content and in the collection index. A filename is an
  address, not a status field.

## The baseline is frozen

Nothing under `baseline/` is ever edited, for any reason, including obvious
typos. It is evidence of what the source model said on a specific date, and its
value is that it can be verified against a tag. Corrections belong in this
project's own documents, and the difference belongs in `extraction/ledger.md`.

## Writing standards

- Say what is true now, and mark what is intended as intended.
- Do not describe unwritten things as available.
- Name the evidence behind a claim, or do not make the claim.
- Prefer a short document that is current over a long one that is stale.
- Write for a competent stranger with no access to the conversation that
  produced the work.

## Verification

This repository has no tooling yet. Until the validator exists, verification is
manual review plus `git diff --check`, and every task states which checks it ran
and which it could not.
