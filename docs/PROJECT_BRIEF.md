# Project Brief

Status: Approved direction for the bootstrap phase. Revised only by an
explicit decision, never by a task in passing.

## What this is

A protocol for keeping long-running work resumable. It moves goals, decisions,
current reality and the next action out of individual memory and chat history
into a small repository state that another competent actor can find, verify and
continue.

The distribution has three separable parts:

1. a normative specification of document ownership and task transitions;
2. reference templates that implement it; and
3. a conformance suite that tests behaviour rather than the presence of files.

## Distribution status

The repository is public open source under the Apache License 2.0, as recorded
in `docs/adr/0001-apache-2.0-open-source-distribution.md`.

This is source publication of a technical preview. It does not claim that the
unwritten specification, templates, profiles or conformance suite exist, and
it is not a versioned protocol release.

## The problem

Long-running work loses continuity because the knowledge that matters is spread
across individual memory, chat logs, unindexed documents, stale plans and
half-finished deliverables.

Adding documents does not fix it. Twenty-five unsorted binders are also
documentation. What a usable system needs is a known entry point, one owner per
truth, a route from a problem to the relevant specification, and a dated record
of what changed and what was verified.

## The technician test

A printer stops working and flashes red. A technician arrives and asks for the
manual and the service history.

Without docs-first: "It might be in one of the twenty-five binders on that
shelf."

With docs-first: "Start with the index in the yellow binder. It points to the
printer specification in the blue binder, page 99." Beside the specification is
a dated note: the same red light was a fuse, here is where the fuse sits, here
is how it was replaced, here is what was verified, and here is who did it.

The technician does not need the organisation's whole history. The system routes
one current problem to the right specification, the relevant prior change and
the next action.

A repository passes the test when a competent newcomer can answer, without
private chat history: what is the active task, which document owns the relevant
truth, what exists now, what changed and when, what was verified, what remains,
and what is explicitly out of scope.

## Goals

- Extract the hardened model as it stands, by transcription rather than
  redesign.
- Keep the core small, domain-neutral and agent-neutral.
- Make conformance testable, in levels, rather than a badge.
- Publish evidence honestly, separating what was observed from what is inferred.

## Non-goals

- A framework, a service, a hosted product or an editor plugin.
- A methodology certification or a badge programme.
- Any claim that the protocol makes AI agents more capable. The defensible
  claim is narrower: it makes work resumable across actors and sessions.
- Simplifying the core before conformance evidence shows the simplification
  costs nothing.

## Evidence position

The model was developed and used across several repositories, technology
stacks, work types and actor families, including work performed by humans and
by more than one AI model family, and by two external users in non-technical
creative production.

That evidence supports these claims and no more:

| Class | Permitted statement |
| --- | --- |
| Observed | The model has been used across named stacks, work types and actor families |
| Supported inference | Repository-owned context contributed to repeatable handoffs and bounded resumption |
| Not yet proven | Universal applicability, causal productivity gain, quantified cost reduction |

The evidence report will publish its counting method before its counts.

## Open decisions

These are not decided, and no task may assume them:

1. The project name, after trademark and registry checks.
2. Whether filenames are normative or only semantic roles are.
3. Which case-study excerpts may be published, and with whose consent.
