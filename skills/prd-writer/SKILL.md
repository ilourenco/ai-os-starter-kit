---
name: prd-writer
description: Writes a problem-first, testable feature PRD under 1,000 words, not a feature spec. Use when the user says "write a PRD", "draft a spec", "product requirements", "product brief", or describes a feature to specify. Reads context for voice, ICP, and this quarter's priorities.
inputs:
  - the feature and a one-sentence hypothesis (required)
  - a specific target user, not "users" (required)
  - at least one customer quote or metric for the problem (required)
---

# PRD Writer (problem-first, testable)

Force a problem-first, testable PRD. Lead with the problem. Be concrete. Read `context/identity.md` and `context/context.md` if present, for voice, ICP, and priorities.

## Refusal

Refuse to write the PRD without all three inputs. Ask for whichever is missing:

1. the feature and a one-sentence hypothesis
2. a specific target user (not "users")
3. at least one piece of evidence for the problem: a customer quote or a metric, plus at least one measurable success metric

A PRD with no user and no evidence is fiction.

## Output structure

This exact order. Problem before any interface or solution detail. Under 1,000 words.

1. **Problem.** One paragraph. Must include the customer quote or the metric. The user pain or business gap, not the solution.
2. **Hypothesis.** One sentence. Why this change will move the metric.
3. **Target user.** The specific user and the job they are trying to get done.
4. **Goals and success metrics.** 2 to 4 measurable outcomes with thresholds (for example activation +X, support tickets -Y, p95 latency under Z). No vague goals.
5. **Scope.** In-scope bullets, max 7.
6. **Non-goals.** What you are deliberately not doing, max 5.
7. **User stories and acceptance criteria.** Each story with Given / When / Then criteria that are testable. Replace "it should be fast" with a number.
8. **Assumptions and constraints.**
9. **Risks.** Max 3, each with a mitigation.
10. **Open questions.** Max 3.

If the user asks for a lightweight version, compress to Problem, Goal metric, Scope in and out, 3 to 5 acceptance criteria, and only the non-functional requirements that are at risk.

## Rules

1. Refuse to write the PRD without a specific target user, a customer quote or metric for the problem, and at least one measurable success metric.
2. Never lead with interface or database detail. Problem first, always.
3. End every PRD with "One claim to verify before kickoff: [the most assertive claim in this doc]." and a note that this PRD is a living document to update after implementation.
