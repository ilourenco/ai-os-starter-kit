# 🚀 Get Started

The step-by-step build. Follow the order. Each step builds one layer and produces specific files. The first three layers fit in one focused afternoon, and the rest take a few minutes each. The whole OS is a one-week job. 🗓️

⭐ **The one instruction that matters most: schedule the Weekly OS Audit (Step 6). Everything else decays without it.**

---

## ✅ Before you start

- Install the kit as a Claude plugin, or clone the repo and work from `templates/`.
- Pick your AI OS folder. This is where `CLAUDE.md`, `context/`, `connections.md`, `MEMORY.md`, and `automations/` will live. Note its absolute path. You will need it for the scheduled tasks.

---

## 📇 Step 1 (Mon): Build your context — Layer 1

Run the **`build-context`** skill.

- It interviews you one question at a time: role, a pasted writing sample for voice, principles, non-negotiables, banned phrases, AI dos and don'ts, this quarter's priorities, your domain, your tools, and the one correction you keep giving.
- **Produces:** `context/profile.md` (renamed to `context/pm.md` if you are a PM), `context/strategy.md`, `context/product-area.md` (PMs only), and `CLAUDE.md` (the router).
- **Done when:** the AI drafts a short message in your voice without being asked. If it does not sound like you, tune one file and rerun. 🎯

## 🔌 Step 2 (Tue): Map your connections — Layer 2

Run the **`map-connections`** skill.

- It lists the connectors actually installed, then asks which three or four you really use, and for each: purpose, trigger, and one cross-tool question.
- **Produces:** `connections.md`, plus a pointer under `## Connections` in `CLAUDE.md`.
- **Done when:** the AI answers a cross-tool question (for example, pulling Slack signal about a Notion pipeline item).

## 🛠️ Step 3 (Wed): Forge your first skill — Layer 3

Run the **`forge-skill`** skill.

- It checks what skills exist, then captures a prompt you have typed three or more times: trigger words, inputs, output format.
- **Produces:** `skills/<name>/SKILL.md` with exactly three rules (one of them a refusal), plus a registered row under `## Skills` in `CLAUDE.md`.
- **Done when:** you invoke the new skill by its trigger and it runs. (Do it twice more for your next two repeated prompts while you are here.)

## ⏰ Step 4 (Thu): Schedule one automation — Layer 4

Run the **`schedule-automation`** skill.

- It captures one recurring deliverable, its cadence, format, and a hard constraint. It refuses to finalize without a constraint. (Good. That is the whole point.)
- **Produces:** a scheduled task, a mirror at `automations/<name>.md`, an updated `automations/README.md`, and a pointer under `## Automations` in `CLAUDE.md`.
- **Done when:** the task is scheduled and you can see it in your task list.

## 🧩 Step 5 (Fri): Seed your memory — Layer 5

Run the **`seed-memory`** skill.

- It proposes three starter memories (one USER, one FEEDBACK, one REFERENCE), each with a why and a date. You approve, edit, or reject each. PROJECT memories require an expiry. 🗓️
- **Produces:** `MEMORY.md` with typed entries, and three memory rules under `## Memory` in `CLAUDE.md`.
- **Done when:** `CLAUDE.md` says "read MEMORY.md before responding" and your approved entries are saved.

## 🔁 Step 6 (Sun): Schedule the Weekly OS Audit — the Loop

Run the **`weekly-os-audit`** skill. **Do not skip this one.** ⭐

- It writes `weekly-os-audit.md` (the audit prompt) and schedules it for every Sunday evening (cron `0 18 * * 0`). The scheduled prompt starts by reading your `CLAUDE.md` and `MEMORY.md` by absolute path, because a scheduled run wakes up with no memory of any chat.
- **Produces:** `weekly-os-audit.md` and a scheduled Sunday task.
- **Done when:** the task is scheduled. From here, the OS audits itself and hands you a few changes each week.

---

## 🎉 After the build

Every Sunday, the audit hands you a short list of proposed changes tagged APPROVE / REJECT / DISCUSS, plus a one-paragraph "what I would do this week." Action it. Within a week of building, you are at Level 5: a context-loaded, connected, skilled, automated, memory-backed AI OS that maintains itself. 🤖
