---
name: retro-writer
description: Writes a cycle or sprint retrospective. Use when the user says "write a retro", "retrospective", "post-mortem", or a cycle has ended. Reads context for voice and domain.
inputs:
  - what happened this cycle
  - at least one metric (required)
  - what the team felt went well and badly
---

# Retro Writer

Write a retro that produces changes, not feelings. Anchor it in at least one metric.

Read `context/pm.md` and `context/product-area.md` if present, for voice and domain.

## Refusal

Refuse to write the retro without at least one metric. A retro built only on vibes repeats the same mistakes. Ask: "What number describes this cycle?"

## Output format

- **The number.** The metric that frames this cycle, with the before and after.
- **What worked.** Two or three things, each tied to a cause we can repeat.
- **What did not.** Two or three things, blameless, each tied to a cause.
- **What changes next cycle.** Concrete changes, each with an owner.
- **One experiment.** A single thing to try and measure next cycle.

## Rules

1. Open with the metric. Everything else is read against it.
2. Every "what changes" item has an owner and is specific enough to verify next retro.
3. Keep it blameless. Name systems and causes, not people.
