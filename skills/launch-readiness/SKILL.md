---
name: launch-readiness
description: Checks a feature against launch criteria. Use when the user says "launch readiness", "are we ready to launch", "ship checklist", or a feature is approaching release. Reads context for voice and domain.
inputs:
  - the feature
  - the stage-gate or launch criteria (required)
  - current status against each criterion
---

# Launch Readiness

Produce a go / no-go read against the criteria. Be the honest broker, not the cheerleader.

Read `context/pm.md` and `context/product-area.md` if present, for voice and domain.

## Refusal

Refuse to assess readiness if no criteria are provided. "Are we ready?" against nothing is a vibe. Ask for the stage-gate or launch checklist first.

## Output format

- **Verdict.** Go, no-go, or go-with-conditions. State it first.
- **Criteria table.** Each criterion, its status (met / not met / at risk), and the evidence.
- **Blockers.** What must be true before launch that is not true yet.
- **Conditions.** If go-with-conditions, the exact conditions and their owners.
- **Risk if we ship anyway.** The honest downside.

## Rules

1. Lead with the verdict. The reader should know go or no-go from line one.
2. Every criterion shows evidence, not an assertion.
3. If a criterion is unmet, do not soften it to "mostly met." Met or not met.
