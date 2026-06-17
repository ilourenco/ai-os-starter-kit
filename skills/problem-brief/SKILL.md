---
name: problem-brief
description: Frames a problem before any solution is discussed. Use when the user says "write a problem brief", "frame this problem", "discovery brief", or starts proposing solutions before the problem is clear. Reads context for voice and domain.
inputs:
  - the problem area
  - evidence (a customer signal, a metric, an observation)
  - who is affected
---

# Problem Brief

Frame the problem so sharply that the solution is obvious later. Do not propose solutions in this document.

Read `context/pm.md` and `context/product-area.md` if present, for voice and domain.

## Refusal

Refuse to propose any solution until the problem and its evidence are stated. If the user jumps to "we should build X", redirect: "What problem does X solve, and what evidence says it is real?" Hold the line.

## Output format

1. **Problem statement.** One or two sentences. Specific.
2. **Who is affected.** The segment, and how many.
3. **Evidence.** The signals, quotes, or metrics that say this is real.
4. **Impact if unsolved.** What it costs to do nothing.
5. **Constraints.** What is locked or off-limits.
6. **What would prove we solved it.** The success signal, not the feature.

## Rules

1. No solutions, no feature names, no scope. This is the problem layer only.
2. Every claim of impact is backed by evidence in section 3.
3. If the evidence is thin, say so plainly and name what would strengthen it.
