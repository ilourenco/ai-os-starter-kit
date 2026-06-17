---
name: weekly-os-audit
description: Builds and schedules the Loop, the keystone of the Personal AI OS. Use when the user says "set up the weekly audit", "schedule the loop", "weekly-os-audit", or has finished building the five layers. Writes the audit prompt, then schedules it for every Sunday evening.
creates:
  - weekly-os-audit.md (the audit prompt, mirror of the scheduled task)
  - schedules the Weekly OS Audit (cron 0 18 * * 0)
---

# Weekly OS Audit (the Loop)

You are building the keystone. Five layers without the loop is a stack, and a stack decays. This skill creates the one scheduled task that scans all five layers every week and proposes a few changes.

## Write the audit prompt

Create **`weekly-os-audit.md`**. It uses `CLAUDE.md` as the index and checks each layer:

- **Context**: files that are stale or over 500 words.
- **Connections**: any connection unused in the last 30 days.
- **Skills**: prompts the user keeps typing that are not yet skills, and skills unused in the last 30 days.
- **Automations**: any automation unread in 14 days or running past its stated constraint.
- **Memory**: entries that are contradictory, expired, or unused.

The audit must:

1. Propose **at most 5 changes per layer**, each tagged **APPROVE / REJECT / DISCUSS**.
2. Append every **REJECT** to `MEMORY.md` (as a FEEDBACK entry) so the same change is not proposed again next week.
3. End with a one-paragraph **"what I would do this week."**

Keep proposals concrete. "Trim context/pm.md from 640 to under 500 words" beats "context could be tighter."

## Schedule it

Schedule the audit for **every Sunday evening** using cron `0 18 * * 0`.

Because a scheduled run starts with no memory of any chat, the scheduled prompt must be self-contained. Begin it with:

> "Read [absolute folder path]/CLAUDE.md and MEMORY.md first, then run the Weekly OS Audit defined in weekly-os-audit.md."

Replace `[absolute folder path]` with the real path to the user's AI OS folder.

## Confirm

Confirm the task was scheduled, report the cron and the next run time, and tell the user plainly: the loop is the single most important step in the kit. The OS now maintains itself.
