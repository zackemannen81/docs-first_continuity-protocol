# Task Workflow

## States

```text
Draft → Ready → In Progress → Complete
                     ↓
                   Paused
                     ↓
                In Progress

Draft / Ready / In Progress / Paused
  → Cancelled or Superseded
```

`Draft` is editable. `Ready` freezes the charter: goal, primary deliverable,
scope, out-of-scope, definition of done and minimum verification gates.
The necessity gate's contract references, intended outcomes and planned checks
freeze with the charter; an approach may be refined only within those bounds.

A frozen charter is superseded, never rewritten. If the goal turns out to be
wrong, archive the task as `Superseded` and charter its replacement. Rewriting a
frozen charter into a different task destroys the only record of what was
actually agreed.

## Necessity Gate

Every substantive change must be necessary to enable, fix, protect or verify an
observable outcome in the current approved Core Contract in
`docs/PROJECT_BRIEF.md`, and fit the active task's frozen charter. If either
link is missing, do not implement that change. Route the gap using the existing
discovery rules below. Independent authorized work may continue.

Before Ready, record these four answers in the task charter for each coherent
change or group serving one outcome:

1. **Authority:** name the exact contract clause and any accepted constraint
   refining it. Pin the Git revision containing the reviewed contract.
2. **Behavior and necessity:** name the observable outcome and what would fail,
   remain unsupported or remain unverified if the change were omitted. State
   the concrete failure or risk, not a generic quality label.
3. **Smallest sufficient change:** choose the simplest credible approach meeting
   that outcome and current constraints; explain any material extra mechanism.
4. **Verification:** name a test, example or review that distinguishes success
   from failure. Put actual results and omissions in the existing Verification
   section.

Missing authority or behavior fails the gate. An undefined approach or check
leaves planning incomplete. A reference, shared keyword or filled field alone
does not establish necessity. Review the reasoning and observable behavior.

### During work and completion

Reuse the recorded argument; routine technical choices inside its authority
and scope need no new owner approval or per-file form. A necessary in-scope
checklist step may add a supporting argument in mutable notes; it cannot add a
new contract outcome to a frozen charter. Record refinements to the initial
approach in those notes rather than rewriting the gate.

Recheck before adding new behavior, dependencies, policy, fallbacks,
compatibility promises or material mechanisms. On resumption and integration,
check whether the contract has changed. Revalidate affected work against the
current accepted contract; a pinned old revision records the agreement but
cannot override a new boundary. Record successful revalidation in mutable notes;
route conflicts through pause or supersession without rewriting the charter.

Before completion, compare the actual changes with the gate arguments. Route
or remove unjustified additions. Do not weaken the contract or checks to make
the implementation pass. New product requirements need an explicit direction
decision before dependent implementation; existing owner authorization need
not be requested again.

### Engineering judgment

Extensibility, robustness, architectural elegance and future-proofing are not
independent requirements. Hypothetical abstractions, generalized infrastructure,
invented prioritization and fallbacks that change semantics fail without a
current required outcome. Compatibility needs an existing supported behavior
or an accepted migration obligation. Multiple representations need a concrete
purpose, one canonical owner and an explicit derivation or reconciliation rule.

Tests, security controls, migrations, recovery and refactoring pass when they
protect or verify a named outcome against a concrete risk and fit the charter.
"Smallest" means least unnecessary mechanism consistent with correctness and
current obligations, not fewest lines or a globally optimal solution.

Documentation repairs may use one concise argument for related corrections.
Bounded research may resolve an uncertainty needed by a contract clause; its
evidence or decision input does not authorize implementing the explored design.
If existing behavior contradicts the contract, record the discrepancy and scope
the fix or seek a direction decision when intent is unclear. Existing code
neither supplies authority nor justifies indiscriminate deletion.

The gate is a required review practice. Structural checks can establish that
references and evidence exist; they cannot prove a change is necessary. Existing
safety obligations still apply. A separate pilot or evidence programme is not
a prerequisite for applying this adopted rule.

## Task Identity

A task identity is an address. It appears in the active charter, the archive
filename, journal entries, branch names, commit messages and pull request
titles, and several of those cannot be rewritten afterwards.

Claim the identity in `docs/TASK_IDS.md` and merge that claim to `main` before
the charter moves to `Ready`. Append one row at the end of the table; never
insert into the middle and never sort. Two people claiming at the same moment
then edit the same region and the second gets a merge conflict rather than a
silent duplicate.

The register cannot prevent the race. It converts it into a conflict, which is
the only reliable outcome available between actors who cannot see each other's
branches.

The register allocates identity only. It carries no status column: task state
already has owners in `docs/CURRENT_TASK.md` and `docs/finished/`, and a
trunk-level statement about active work would contradict the one-active-task
rule.

## Routing Discovered Work

Every discovery gets one of four destinations. Choosing none of them, and
simply doing the work, is how a frozen charter erodes.

```text
Is it required by the frozen charter?
├─ Yes → add a checklist step and do it
└─ No
   ├─ Does it block the charter?
   │  ├─ Yes → pause the parent, activate a bounded child task
   │  └─ No
   │     ├─ In project scope, later → docs/backlog/
   │     └─ Outside project scope   → docs/concepts_sandbox/
```

A backlog proposal records discovery context, proposed outcome, why it is
outside the active charter, dependencies and suggested verification. Add it to
`docs/backlog/README.md` in the same change; an unindexed proposal is invisible.

Resolving a proposal updates its `Status:` line and its index row. It never
renames or moves the file, because journal entries and archived tasks cite
proposals by path and cannot be edited to follow a rename.

## Pause

A pause records what blocked the work, what the next step is, which
verifications did not run, and the condition that resumes the task. Move the
frozen parent to `docs/paused/` and keep its identity, goal and definition of
done unchanged.

## Completion

- Review the actual change set against the Necessity Gate and frozen charter.
- Verify in proportion to risk. State what was not verified and why.
- Update every affected owning document in the same change.
- Archive the task under `docs/finished/` as `DFC-NNNN_task-slug.md`, unmodified.
- Restore `docs/CURRENT_TASK.md` from the template, or fill it with the next
  approved task.
- Add a dated, signed journal entry.

A task is not complete because the work feels done. It is complete when the
repository shows what was produced, what was verified, and what the next actor
should do.
