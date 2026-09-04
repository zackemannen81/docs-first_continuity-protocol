# Core contract and necessity gate

Status: Proposed

Created: 2026-09-05
Last updated: 2026-09-05
Prepared by: Codex
Task identity: not allocated; implementation is not activated.

## Definition

> Every substantive change must be necessary to enable, fix, protect or verify
> an observable outcome in the current approved core contract, and must fit the
> active task's frozen charter. If either link is missing, do not implement the
> change. Route the gap through the existing task workflow.

The **Core Contract** is a short, authoritative description of what the work
must accomplish now, including essential behavior and boundaries. The
**Necessity Gate** records why a proposed change is needed to satisfy it.
Software projects may call these the **Core Product Contract** and
**Implementation Gate**; the protocol terms also cover documents, research,
operations and creative work.

This is proposed adoption text, not an operating rule or conformance claim.
The [decision proposal](../adr/0002-core-contract-and-necessity-gate.md) records
the boundary to settle before adoption.

## Discovery, scope and evidence

The owner requested this preparation after describing implementations that
introduced complexity and prioritization absent from the intended behavior.
That report motivates the proposal. Its source code, runtime results and
reported code reductions were not independently verified here. Examples below
are newly written; private source material is not reproduced.

Observed here: the workflow freezes task scope, but the workflow and task
template do not require a necessity argument against current purpose. An
unnecessary feature can enter a Draft charter and survive its freeze.

Hypothesis: this gate exposes invented requirements earlier without obstructing
ordinary engineering judgment. Its effect on actual work remains unmeasured.
It must not inherit the baseline's history of use.

DFC-0001 transcribes CORE rows from the extraction ledger. This proposal adds
behavior absent from those rows. It is in project scope but is not required to
transcribe the baseline, so it belongs in a separate adoption task. The
proposal keeps this path after activation; update its status and index.

## One owner, a short contract

Use a named section of the document already owning approved direction. Here,
the proposed location is a `Core Contract` section in `docs/PROJECT_BRIEF.md`.
Do not create a second product truth in another file. Other adopters can map the
role to their existing product definition; this does not settle the open
decision about normative filenames.

Keep the contract to roughly one page: purpose and beneficiary, a few observable
outcomes or invariants with stable local clause IDs, explicit boundaries, and
the approving decision. Retired IDs are not reused for different meanings.
Git supplies revision history; no new versioning system is needed.

The contract states approved required behavior. Current implementation and gaps
stay in current status, design in the system document, and history in the
journal. Roadmap aspirations cannot authorize current work. Accepted constraints
can refine clauses; cite both. "Quality" or a link to the entire brief supplies
no necessity argument.

### Candidate contract for this repository

The following is proposed text. CC identifiers are local to this candidate,
not new C-series protocol requirements or adopted authority.

> The docs-first continuity protocol keeps long-running work resumable by
> placing its approved purpose, current state, decisions and next action in
> repository-owned records another competent actor can find and use.
>
> - **CC-01 — Find the authority.** From the entry point, find the active task
>   and its relevant owning records; distinguish approved direction, current
>   reality, history and undecided material.
> - **CC-02 — Keep work bounded.** Each branch holds at most one active task.
>   Its charter remains fixed after Ready; discoveries receive an explicit
>   route rather than silently changing the agreed outcome.
> - **CC-03 — Leave a usable handoff.** Record changes, verification and
>   omissions, remaining work and any resume condition, so a competent successor
>   can continue without private conversation history.
> - **CC-04 — Preserve retrieval.** Cited records retain their addresses, and
>   collection members remain discoverable under declared conventions.
> - **CC-05 — Make claims inspectable.** Rules and conformance claims identify
>   their origin and checking means; observed use, inference and new hypotheses
>   remain distinguishable.
>
> The core stays agent-neutral and domain-neutral. Its intended distribution
> comprises a specification, reference templates and a conformance suite;
> current status reports their actual availability. It does not build a runtime
> framework or claim that adopting the protocol makes agents more capable.

This restates approved purpose. Mere association with one broad clause does
not authorize a feature; the gate must establish a specific need.

## Proposed gate

Before Ready, answer these for each coherent change or group serving one
outcome. Reuse the argument during implementation; no form per line or tool call.

1. **Authority:** Which exact core-contract clause requires this? Name the
   owning document and clause, plus any accepted constraint that refines it.
2. **Behavior and necessity:** What observable outcome does this enable, fix,
   protect or verify? What would fail, remain unsupported or remain unverified
   if it were omitted? Name the concrete failure or risk.
3. **Smallest sufficient change:** What is the simplest credible implementation
   meeting that outcome and existing constraints? Explain material extra
   mechanisms relative to that option.
4. **Verification:** Which check, example or named review distinguishes success
   from failure? Put actual results in the existing Verification section.

Missing authority or behavior fails the gate. A missing sufficient approach or
check leaves planning incomplete. Filled fields, shared keywords and task scope
alone cannot establish necessity. Review the reasoning and actual behavior.

Both contract necessity and frozen task scope are required. Ordinary technical
choices supported by both need no new owner approval. Recheck when an approach
introduces new behavior, dependencies, policy, fallbacks, compatibility promises
or material mechanisms. Before completion, compare the actual diff with the
arguments; route or remove unjustified additions. Do not weaken the contract or
tests to make the implementation pass.

"Smallest" means least unnecessary mechanism consistent with correctness and
current obligations, not fewest lines, a fixed complexity budget or proof of a
global optimum. Discuss alternatives only when extra mechanism needs explaining.

### Task template insertion

Place this inside the Task Charter, before Minimum Verification Gates:

```markdown
### Necessity Gate

Contract: <owning document and section>
Contract revision: <Git commit containing the reviewed contract>

| Change | Clause and accepted constraint | Outcome; consequence if omitted | Smallest sufficient change | Planned check |
| --- | --- | --- | --- | --- |
| <coherent change> | <exact reference> | <enable / fix / protect / verify; concrete consequence> | <bounded approach> | <test or named review> |
```

References, intended outcomes and planned checks freeze with the charter. The
approach column records the initial plan; mutable implementation notes may
refine it within those frozen boundaries. Results belong in Verification.

A changed upstream contract requires revalidation before dependent work
continues, including on resumption or integration. A pinned revision records the
agreement; it cannot override a newly accepted boundary. Record revalidation in
mutable notes. Semantic conflicts follow existing pause/supersede routing; do
not rewrite the frozen record.

## Boundaries and routing

| Situation | Required handling |
| --- | --- |
| Hypothetical abstraction, provider or generalized infrastructure | Fail without a current need. Extensibility, elegance and future-proofing are not independent requirements. |
| New ranking policy, early return or fallback | Fail if it changes agreed behavior without authority. Implementation convenience cannot invent product semantics. |
| Parallel representations | Require a current need, one canonical owner and a defined relationship, such as a derived index needed for an approved lookup bound. |
| Compatibility layer | Require existing supported behavior or an accepted migration obligation, not an imaginary future consumer. |
| Tests, security, migrations or recovery | Pass when protecting or verifying a named outcome against a concrete risk within the charter. No blanket quality exemption. |
| Refactoring | Require a necessary change or concrete defect/risk and a behavior-preservation check; architectural preference alone fails. |
| Documentation correction | One concise argument may cover related repairs to accuracy, discoverability or handoff. |
| Research | A bounded investigation may resolve an uncertainty needed by a clause. Evidence or a decision input is its deliverable; explored implementations gain no authority. |
| Code contradicts the contract | Record the discrepancy and charter a fix, or seek a direction decision if intent is unclear. Existing code neither proves authority nor warrants indiscriminate deletion. |
| Genuine new product need | Obtain an explicit direction decision first. An implementer cannot add a convenient clause just to justify their change. |

Use the existing routes: in-charter checklist step, blocking prerequisite with
pause and bounded child, in-project backlog, or excluded concept. Hold the
affected change when authority is missing; independent authorized work may
continue. No new lifecycle state is needed.

## Acceptance scenarios

These are synthetic review fixtures with expected verdicts, not executed runtime
tests. Review the arguments, not just fields. During adoption, compare the
existing workflow and the proposed gate against the same fixtures.

| Case | Setup / proposed change | Expected result and evidence |
| --- | --- | --- |
| NG-01 | CC-03; fix a handoff template omitting skipped verification and next action | Pass in a scoped task; a completed sample contains both. |
| NG-02 | CC-03; build an automatic scheduler because it might help continuity | Fail: no required current outcome needs it; a runtime framework crosses the boundary. |
| NG-03 | Synthetic contract: return all matching records from three classes; add an early return after the first class | Fail: policy suppresses required results. A fixture matching all three must retain all three. |
| NG-04 | Synthetic contract: retain saved records; add a necessary schema migration | Pass within a migration charter with old-data upgrade and restart checks. |
| NG-05 | Synthetic contract: only owners may read private records; add an ownership check | Pass with a cross-owner read refusal check; "more secure" alone fails. |
| NG-06 | All fields are filled; CC-03 is cited with only "robustness" as necessity | Fail: no concrete consequence or distinguishing check. |
| NG-07 | A valid CC-04 index improvement is found in an unrelated frozen task | Route to backlog; contract relevance does not enlarge task scope. |
| NG-08 | Implementer broadens the contract to justify an unsupported fallback | Fail; propose a direction decision and hold dependent work. |
| NG-09 | Contract changes after Ready, invalidating planned behavior | Revalidate and pause or supersede as appropriate; the old revision cannot authorize invalid behavior. |
| NG-10 | Repair a contradictory sentence in an approved non-software brief-editing task | Pass with one grouped argument and before/after review; no per-line form or software build. |
| NG-11 | Bounded investigation compares two ways to preserve retrieval addresses under CC-04 | Pass with a question, bounded investigation and decision input; no implicit production implementation. |
| NG-12 | Gate fields pass but the diff adds an unrecorded second truth owner | Fail completion review; remove the addition or justify a canonical/derived relationship within authority and scope. |

NG-03 through NG-05 use invented product contracts. They add no retrieval,
storage or security semantics to this protocol's core.

## First adoption and shipping plan

Start with a local trial in this repository's working documents. It is a useful
bounded deliverable without building tooling or completing the distribution.

| Owning surface | Adoption change |
| --- | --- |
| Decision record | Explicitly accept or revise the proposed boundary; record local-trial status and new-rule provenance. |
| Project brief | Add the approved contract and explicit permission for this local evolution alongside baseline transcription. |
| Entry point | Route to the contract and require the gate; reference the workflow rather than duplicate its procedure. |
| Task workflow | Add the check before Ready, recheck triggers and final diff review with existing routing. |
| Local task template | Insert the compact gate. This repository's operating template is distinct from shipped profile templates. |
| System document, status, map and journal | Describe actual ownership and adoption state, checks and limitations. |

Suggested adoption charter:

- **Goal:** make substantive changes here explainably necessary for the approved
  core contract and bounded by the existing task charter.
- **Primary deliverable:** the working docs-first instance with an adopted
  contract and gate usable by the next actor from the repository.
- **In scope:** the surfaces above, scenario review, and a sample charter
  applying the gate to adoption itself.
- **Out of scope:** baseline edits, extraction-ledger rewrites, the full
  specification, distributed profiles/templates, validator/runtime code,
  automated semantic judgments, mass code removal, releases and announcements.
- **Done:** one contract owner; entry and workflow reach it; the template records
  all four answers; a sample demonstrates use; every scenario has an actual
  verdict and explanation; owning documents and archived task report checks.
- **Verification:** reference and fence review, scenario verdicts, a
  repository-only handoff walkthrough, immutable-file checks and
  `git diff --check`. A walkthrough by the implementing actor is self-review,
  not evidence of an independent newcomer test.

Activation requires an explicit direction decision and a new identity claimed
on main before Ready. Re-read register and archive then; no future DFC number
is reserved here. Preserve DFC-0001 separately, using separate branches if both
tasks proceed. The adoption can run before the baseline specification is done.

Later distribution needs a separate extension document and adoption mapping
after the baseline specification defines its requirement and conformance
scheme. Follow the ledger's conservative classification rule: try an opt-in
extension before deciding on core promotion. Do not fabricate baseline rows or
silently renumber C-series destinations. Publication requires its own explicit
release decision and verified release work.

Opt-in concerns adopting the extension. Once adopted, its gate is mandatory for
substantive changes; it is not an optional suggestion on each task.

If later justified, a checker can validate structure, references and required
evidence. Actual necessity remains a named review judgment. This proposal does
not justify a scoring engine, dependency service or agent orchestrator.

## Handoff

The dated journal entry records checks on this preparation. The adoption gates
above remain future work. Next: review the proposed decision and candidate
contract, then activate bounded local adoption if accepted. Accepting this
design alone does not create a versioned protocol release.
