# 🧠 AI OS Starter Kit

**Stop re-explaining yourself to your AI every single morning.**

Build a Personal AI Operating System once: five layers, one weekly loop. Give your AI your context, your tools, your patterns, and your approved memory, then let a single scheduled task keep the whole thing current while you do actual work.

This kit is two things at once: an installable Claude plugin 🔌 and a clone-and-fill template repo 📁. It ships with ready-to-use skills for product managers, so it earns its keep on day one (no six-month discovery phase required).

---

## 🏗️ The model: five layers, one loop

The router file, `CLAUDE.md`, is the spine. It gets read first and indexes every layer. Each layer registers itself there. (No router, no OS. It is just five piles your AI does not know to read.)

| Layer | What it is | The trap 🪤 | The discipline ✅ |
|---|---|---|---|
| 1. **Context** 📇 | Files the AI reads every time: who you are, your voice, your strategy, your domain | Bloat. A 2,000-word profile is wallpaper | 500 words per file |
| 2. **Connections** 🔌 | The tools the AI can reach (Slack, Notion, Linear, Calendar) | Sprawl. Twelve authorized, three actually used | Map the few you use. Three beats twelve |
| 3. **Skills** 🛠️ | Reusable prompt patterns saved as files, invoked by trigger | Writing skills you never touch again | Write it the third time you type it. Register every one in the router |
| 4. **Automations** ⏰ | Scheduled prompts that run without you | Unconstrained output you quietly stop reading | Every automation gets a hard constraint. An index lists them all |
| 5. **Memory** 🧩 | Typed, approved facts that persist (USER, FEEDBACK, PROJECT, REFERENCE) | Default-on memory with no audit, quietly filling with half-truths | Approve every save, type it, write the why, load it every time |

🔁 **The Loop: the Weekly OS Audit.** One scheduled task scans all five layers every Sunday and proposes a few changes. It is the keystone. Five layers without the loop is a stack, and a stack decays (context goes stale, skills pile up, memory contradicts itself).

📖 Full theory: [`framework/ai-os.md`](framework/ai-os.md).

---

## ⚡ 60-second quickstart

1. Install the kit (below) or clone it.
2. Run the **`build-context`** skill. Answer the interview.
3. Watch your AI draft a message that actually sounds like you, unprompted. 🎉 That is Layer 1 working.
4. When you are ready, run **`weekly-os-audit`** to schedule the loop. That is the OS maintaining itself while you sleep. 😴

---

## 📦 Two ways to use it

🔌 **As a Claude plugin.** Install it so the skills are available by trigger. Run `build-context` first, then the rest, then `weekly-os-audit` last.

📁 **As a template.** Clone the repo, copy the files in `templates/` into your working folder, and fill them in by hand using the structure as a guide. The `CLAUDE.md` template already carries the five section headers and the always-read-memory rule.

---

## 🔨 Build order

Six builder skills. Run them in order. Each builds one layer and registers it in the router.

1. 📇 `build-context` — your profile, strategy, product area, and the router.
2. 🔌 `map-connections` — the few tools you actually use.
3. 🛠️ `forge-skill` — turn a prompt you keep retyping into a registered skill.
4. ⏰ `schedule-automation` — one recurring deliverable with a hard constraint.
5. 🧩 `seed-memory` — three approved, typed starter memories.
6. 🔁 `weekly-os-audit` — schedule the Sunday loop. **This is the one you do not skip.**

---

## 🧰 Ready-to-use PM skills

Opinionated, each with a clear output format and at least one refusal, so your AI asks instead of guessing past a missing input.

| Skill | What it does | It refuses without... |
|---|---|---|
| 📝 `prd-writer` | A feature PRD under 1,000 words | a target user and a customer quote or metric |
| 🔍 `problem-brief` | Frames a problem before any solution | the problem and evidence stated first |
| 📣 `status-update` | A tight, scannable status | a customer signal source |
| 🚀 `kickoff-brief` | A five-paragraph sprint or feature kickoff | a real goal (not "build the feature") |
| 🤝 `one-on-one-prep` | Commitments, blockers, open decisions | a named person |
| ⚔️ `competitor-teardown` | A battlecard with a verifiable claim | a named competitor and your ICP |
| ✅ `launch-readiness` | A go / no-go against stage-gate criteria | criteria to check against |
| 🔄 `retro-writer` | What worked, what did not, what changes | at least one metric |

---

## 📈 Maturity ladder

Where you are, and what good looks like next.

- **0. Cold start** 🥶 — re-explaining yourself every session.
- **1. Context loaded** 📇 — the AI writes in your voice without being told.
- **2. Connected** 🔌 — the AI reaches your real tools and answers cross-tool questions.
- **3. Skilled** 🛠️ — your most-repeated prompts are registered skills.
- **4. Automated** ⏰ — at least one constrained automation runs on a cadence.
- **5. Self-maintaining** 🔁 — the Weekly OS Audit runs every Sunday and you action its proposals.

Most of the value shows up at Level 2. Most of the durability shows up at Level 5.

---

## 🗓️ The one-week plan

You do not need a quarter. You need a week. (Honestly, a focused afternoon gets you most of the way.)

- **Mon** 📇 — `build-context`. Stand up the router and your context files. Done when your AI drafts something in your voice.
- **Tue** 🔌 — `map-connections`. Map your three or four real tools.
- **Wed** 🛠️ — `forge-skill` on the prompt you type most. Then do it twice more for your next two.
- **Thu** ⏰ — `schedule-automation`. One deliverable, one hard constraint.
- **Fri** 🧩 — `seed-memory`. Approve three starter memories.
- **Sun** 🔁 — `weekly-os-audit`. Create and schedule the loop. From here, the OS audits itself.

By the end of week one you are at Level 5: context-loaded, connected, skilled, automated, memory-backed, and self-maintaining. 🎯

📋 Step-by-step version with what each step produces: [`GET-STARTED.md`](GET-STARTED.md).

---

## 📄 License

MIT. See [`LICENSE`](LICENSE). Take it, fork it, make it yours.
