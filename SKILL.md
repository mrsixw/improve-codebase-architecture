---
name: improve-codebase-architecture
description: Survey a repository for concrete architecture and module-deepening opportunities, then present a prioritized report without changing production code.
disable-model-invocation: true
---

# Improve Codebase Architecture

This is a read-only survey that produces candidates for later design or implementation work.

## Workflow

1. Establish the repository's stack, entry points, dependency direction, and existing architecture documents.
2. Find shallow or pass-through modules, duplicated boundaries, scattered responsibilities, and difficult test seams.
3. Separate evidence from design judgement and cite relevant files and lines.
4. Rank candidates by user impact, change locality, risk, and effort.
5. Present a concise report and let the user choose one candidate.
6. Stop after the survey unless the user explicitly requests a follow-up design or implementation.

Do not turn the survey into an unsolicited refactor. Reports should be saved where the user or repository convention specifies.
