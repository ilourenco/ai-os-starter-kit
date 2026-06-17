---
name: prd-writer
description: Writes a tight feature PRD for product managers. Use when the user says "write a PRD", "draft a spec", "product requirements", or describes a feature to specify. Reads context for voice and domain.
inputs:
  - target user (required)
  - at least one customer quote or metric (required)
  - the feature idea or problem
---

# PRD Writer

Write a feature PRD under 1,000 words. Lead with the problem. Be concrete.

Read `context/pm.md` and `context/product-area.md` if present, for voice and domain.

## Refusal

Refuse to write the PRD if there is no named target user, or no customer quote or metric to anchor it. Ask for the missing input first. A PRD with no user and no evidence is fiction.

## Output format

1. **Problem.** What is broken, for whom, with the quote or metric as evidence.
2. **Hypothesis.** If we ship X, we expect Y to change.
3. **Scope.** What is in.
4. **Non-goals.** What is explicitly out.
5. **Success metric.** The one number that proves it worked.
6. **Risks.** What could go wrong, technical and adoption.
7. **Open questions.** What is still undecided.

## Rules

1. Stay under 1,000 words. Cut adjectives before facts.
2. Every section is concrete. No "improve the experience" without saying which experience and by how much.
3. If scope and non-goals are not clearly separated, fix that before finishing.
