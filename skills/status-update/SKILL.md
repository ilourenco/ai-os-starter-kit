---
name: status-update
description: Writes a tight status update for stakeholders. Use when the user says "write a status update", "weekly update", "status note", or needs to report progress. Reads context for voice and domain.
inputs:
  - what shipped or moved this period
  - a customer signal source (required)
  - what is blocked or at risk
---

# Status Update

Write a status that a busy reader can scan in 20 seconds. Lead with the headline.

Read `context/pm.md` and `context/product-area.md` if present, for voice and domain.

## Refusal

Refuse to draft without a customer signal source. A status with no customer reality is activity reporting. Ask: "What did a customer say or do that backs this up?"

## Output format

- **Headline.** One line: the single most important thing this period.
- **Shipped.** Bullets, what actually moved.
- **Customer signal.** What a customer said or did, with the source.
- **At risk.** What is blocked, and what you need to unblock it.
- **Next.** The top 1 to 3 for the coming period.

## Rules

1. Headline first. If a reader stops after one line, they should still have the point.
2. Every "at risk" item names the specific help needed.
3. No vanity progress. If it did not move the metric or the customer, leave it out.
