---
name: schedule-automation
description: Builds Layer 4 (Automations) of the user's Personal AI OS. Use when the user says "schedule an automation", "set up a recurring task", "schedule-automation", or describes something they want delivered without asking. Drafts a self-contained scheduled prompt with a hard constraint, schedules it, and indexes it.
creates:
  - automations/<name>.md (mirror of the scheduled prompt)
  - updates automations/README.md (the index)
  - updates CLAUDE.md (## Automations section)
---

# Schedule Automation (Layer 4)

You are building Layer 4. An automation is a scheduled prompt that runs without the user. The failure mode is output nobody reads, so the constraint is the point.

## Interview

Ask the user, one question at a time:

1. **What do you want delivered without having to ask for it?** (a Monday digest, a Friday metric snapshot, a weekly competitor scan).
2. **Cadence.** How often, and at what time? Convert this to cron.
3. **Format.** What should land, and where (a Slack channel, a file path, an email)?
4. **The constraint.** What is the hard limit that forces a decision? Examples: top 3 only, one paragraph, flag only the single thing that changed, no more than 200 words.

**Refuse to finalize the automation without a constraint.** If the user will not name one, propose one and get their yes. An automation with no constraint becomes noise.

## Draft the scheduled prompt

Write a **fully self-contained** prompt. A scheduled run starts with no memory of this chat, so the prompt must stand alone. It must:

- Begin by reading the user's folder context: "Read [absolute path]/CLAUDE.md and [absolute path]/MEMORY.md first."
- Name the connector it uses (do not say "the usual tool").
- State the exact output path or destination.
- Carry the hard constraint in the prompt text itself.

## Schedule it

Use the scheduling tool to create the task at the agreed cadence. Confirm it was created and report the schedule back to the user.

## Mirror and index

1. Save a copy of the final prompt to **`automations/<name>.md`** so the automation survives even if the scheduler is lost.
2. Update **`automations/README.md`** (the index): add a row with **name**, **cadence**, **output destination**, and **constraint**.
3. Update **`CLAUDE.md`** under the `## Automations` header with a pointer: "My automations are indexed in ./automations/README.md."
