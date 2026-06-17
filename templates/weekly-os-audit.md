# Weekly OS Audit

The keystone. This prompt is run once a week by a scheduled task to keep the AI OS alive. `weekly-os-audit` writes the real version and schedules it for Sunday 18:00 (cron `0 18 * * 0`).

Because a scheduled run starts with no memory of any chat, the scheduled prompt is self-contained and begins by reading the router and memory.

---

**Scheduled prompt (replace the path):**

> Read [absolute folder path]/CLAUDE.md and [absolute folder path]/MEMORY.md first, then run the Weekly OS Audit below.

---

## The audit

Use `CLAUDE.md` as the index. Check each layer and propose changes.

1. **Context.** Flag any file that is stale or over 500 words.
2. **Connections.** Flag any connection unused in the last 30 days.
3. **Skills.** Flag prompts I keep typing that are not yet skills, and skills unused in the last 30 days.
4. **Automations.** Flag any automation unread in 14 days or running past its stated constraint.
5. **Memory.** Flag entries that are contradictory, expired, or unused.

## Rules

1. Propose at most 5 changes per layer. Tag each one APPROVE / REJECT / DISCUSS.
2. Append every REJECT to `MEMORY.md` as a FEEDBACK entry, so it is not proposed again.
3. Keep proposals concrete. "Trim context/pm.md from 640 to under 500 words" beats "context could be tighter."

## Close

End with one paragraph: "what I would do this week." Pick the single highest-leverage change and say why.
