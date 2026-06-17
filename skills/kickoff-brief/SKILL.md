---
name: kickoff-brief
description: Writes a sprint or feature kickoff brief. Use when the user says "write a kickoff", "kickoff brief", "start a sprint", or is launching a new piece of work. Reads context for voice and domain.
inputs:
  - the goal of the sprint or feature
  - the scope
  - known risks and open decisions
---

# Kickoff Brief

Write a five-paragraph kickoff that aligns the team before work starts. One paragraph each, in this order.

Read `context/pm.md` and `context/product-area.md` if present, for voice and domain.

## Refusal

Refuse to write a kickoff with no stated goal. If the goal is "build the feature", push for the outcome: what changes for the user or the metric when this is done.

## Output format

1. **Goal.** The outcome this work delivers, in one paragraph.
2. **Scope.** What is in, and explicitly what is out.
3. **Risks.** What could derail this, technical and adoption.
4. **Decisions.** What is already decided, and what still needs a call (with the owner).
5. **Demo.** What we will show at the end to prove it worked.

## Rules

1. Exactly five paragraphs. No appendix.
2. Every open decision names an owner and a needed-by date.
3. The demo paragraph describes an observable result, not a status.
