---
name: improve-codebase-architecture
description: Survey a repository for concrete architecture and module-deepening opportunities, then present a prioritised report without changing production code.
---

# Improve codebase architecture

Produce an evidence-backed shortlist of architecture improvements. This skill
is read-only with respect to production code and configuration, and it never
implements a candidate. The only permitted write is the report at a path the
user specifies. Do not turn an exploratory review into an unsolicited refactor.

## Survey the as-built system

Establish the stack, entry points, ownership boundaries, dependency direction,
runtime paths, tests, and existing architecture records. Sample enough callers
to distinguish a recurring problem from an isolated awkward file.

Look for scattered policy, repeated coordination, unclear lifecycle ownership,
pass-through layers, duplicated boundaries, hidden side effects, and seams that
make important behaviour difficult to verify. Separate observed evidence from
design judgement.

## Rank bounded candidates

For each candidate, report:

- the concrete pain and cited evidence;
- the proposed responsibility boundary;
- affected callers and operational behaviour;
- expected benefit;
- migration and regression risk;
- a proportionate validation strategy; and
- impact, locality, confidence, and effort.

Rank recurring, high-impact problems above broad aesthetic rewrites. Include the
survey coverage and unresolved unknowns so the report does not imply exhaustive
knowledge. Scale the report to the repository and omit fields with nothing
material to record.

Let the user choose a candidate. Stop after the report unless they explicitly
request follow-up design or implementation. Do not write a report file unless
the user supplies its location.
