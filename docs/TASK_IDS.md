# Task ID Register

Floor: DFC-0001

This register allocates task identities. It records that a number is taken and
by whom. It never records whether work is in progress, complete or abandoned:
task state belongs to `docs/CURRENT_TASK.md` and `docs/finished/`, and a second
statement about it here would drift from both and would make the trunk claim how
much work is active across the repository.

The prefix `DFC` encodes the descriptive method, not a brand. The project name
is undecided, and an identity that carried the name would need a rename once the
name changed — which the addressing rule forbids, because identities are cited
by records that cannot be edited.

## How to claim

1. The next free identity is one above the highest of this register and
   `docs/finished/`.
2. Append one row at the end of the table below. Never insert into the middle,
   never sort, never group by owner. The append point is the safety mechanism:
   two people claiming at the same moment edit the same region and the second
   gets a merge conflict instead of a silent duplicate.
3. Merge the claim to `main`. The identity is not yours until that lands.
4. Only then move the charter to `Ready`.

## Claims

| Task ID | Title | Owner | Claimed | Work |
| --- | --- | --- | --- | --- |
| DFC-0001 | protocol specification, C-01 to C-18 | unassigned | 2026-08-19 | not started |
| DFC-0002 | core contract and necessity gate | Codex | 2026-09-05 | — |
