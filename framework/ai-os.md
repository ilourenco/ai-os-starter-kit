# The Personal AI Operating System

A Personal AI OS is five layers and one loop. You build it once and maintain it weekly with a single scheduled task. The point is simple: stop re-explaining yourself to your AI every session, and let it act with your context, your tools, your patterns, and your approved memory already loaded.

This document is the theory. The skills in this kit are the practice. Read this once, then run `build-context` and let the builders do the work.

---

## The model: five layers, one loop

```
        ┌─────────────────────────────────────────┐
        │              CLAUDE.md (router)           │
        │   read first, indexes every layer below   │
        └─────────────────────────────────────────┘
              │      │       │        │        │
         Context  Connections  Skills  Automations  Memory
              │      │       │        │        │
        └────────────── The Loop (Weekly OS Audit) ──────────────┘
                    one scheduled task, scans all five
```

The router, `CLAUDE.md`, is the spine. It is read first, it indexes every layer, and each layer registers itself there. Without the router, the five layers are five piles the agent does not know to read.

---

## Layer 1: Context

Files the agent reads at the start of every interaction. Context has two halves. Identity is the personal half: who you are, your voice, your principles, your non-negotiables, the rules the agent must always enforce. Context is the organizational half: your company and stage, the area you own, your ICP, the metric you own, what is locked, what is open.

- **What it does.** Removes the re-explaining tax. The agent already knows your role, your priorities, what is locked, and how you write.
- **The trap: bloat.** Context files grow until they are no longer read closely. A 2,000-word profile is wallpaper.
- **The discipline: 500 words per file.** If a file needs more, split it by topic. Short files get read. Long files get skimmed.

Starter files: `context/identity.md` (the personal half) and `context/context.md` (the organizational half). Build identity first, then context.

---

## Layer 2: Connections

The tools and connectors the agent can reach: Slack, Notion, Linear, Calendar, and the rest.

- **What it does.** Lets the agent pull live signal and act, instead of working from what you paste in.
- **The trap: sprawl.** Twelve connectors authorized, three actually used. The agent guesses wrong about where to look.
- **The discipline: map the few you use.** Three used beats twelve connected. For each connection, write what it is for, when the agent should reach for it, and one cross-tool question it answers.

Starter file: `connections.md`.

---

## Layer 3: Skills

Reusable prompt patterns saved as files the agent invokes by trigger.

- **What it does.** Turns a prompt you keep retyping into a named capability with a fixed output and a refusal rule.
- **The trap: writing skills you never use.** A library of clever skills that sit idle is overhead, not leverage.
- **The discipline: write the skill the third time you type the same prompt.** Register every skill in the router so the agent knows it exists. A skill not in the router is invisible.

Starter files: the seven builder skills (`build-identity`, `build-context`, `map-connections`, `forge-skill`, `schedule-automation`, `seed-memory`, `weekly-os-audit`), plus the ready-to-use product management skills, including `competitor-research` and `prd-writer`.

---

## Layer 4: Automations

Scheduled prompts that run without you.

- **What it does.** Delivers recurring work (a Monday digest, a weekly competitor scan) to a known place on a known cadence.
- **The trap: unconstrained output you stop reading.** An automation that dumps everything becomes noise inside two weeks.
- **The discipline: every automation has a hard constraint, and an index lists them all.** A constraint forces a decision: top 3 only, one paragraph, flag the single thing that changed. The index (`automations/README.md`) keeps the set visible.

Starter file: `automations/README.md`.

---

## Layer 5: Memory

Typed, approved facts that persist between conversations.

- **The four types.**
  - **USER**: durable facts about you (role, company, how you work).
  - **FEEDBACK**: corrections you have given the agent, with the why.
  - **PROJECT**: time-bound facts about current work. Every PROJECT memory carries an expiry date.
  - **REFERENCE**: pointers to external resources (dashboards, docs, tickets).
- **The trap: default-on memory with no audit.** Memory that saves silently fills with half-truths and contradictions you never approved.
- **The discipline: approve every save, type it, write the why, load it every conversation.** The router carries the rule "read MEMORY.md before responding." Nothing enters memory without your yes.

Starter file: `MEMORY.md`.

---

## Verification: the discipline that earns trust

Verification is not a sixth layer. It is the discipline that runs through three places you already have. Skills refuse without their inputs, so a missing input stops the work instead of producing a confident guess. Automations show their sources, so you can check what they tell you. The Weekly OS Audit verifies the whole OS every week. Naming verification out loud is what makes an agentic OS trustworthy, because the parts that act on your behalf are also the parts that check themselves.

---

## The Loop: the Weekly OS Audit

One scheduled task that scans all five layers and proposes a few changes each week. It is the keystone.

Five layers without the loop is a stack, and a stack decays. Context files go stale, connections fall out of use, skills pile up unused, automations drift past their constraint, memory accumulates contradictions. The loop is what keeps the OS alive.

Each week the audit checks:

- **Context**: files that are stale or over 500 words.
- **Connections**: anything unused in 30 days.
- **Skills**: prompts you keep typing that are not yet skills, and skills unused in 30 days.
- **Automations**: anything unread in 14 days or running past its constraint.
- **Memory**: contradictory, expired, or unused entries.

It proposes at most five changes per layer, each tagged APPROVE / REJECT / DISCUSS. Rejections are appended to MEMORY.md so the same change is not proposed again. It ends with a one-paragraph "what I would do this week."

It runs every Sunday evening (cron `0 18 * * 0`). Schedule it. The loop is the single most important step in this kit.

---

## The maturity ladder

Where you are, and what good looks like next.

1. **Level 0, Cold start.** Every session begins by re-explaining who you are. No persistent files.
2. **Level 1, Context loaded.** A profile and a router exist. The agent writes in your voice without being told to.
3. **Level 2, Connected.** The agent reaches your real tools and answers cross-tool questions.
4. **Level 3, Skilled.** Your three or four most-repeated prompts are skills with refusals, registered in the router.
5. **Level 4, Automated.** At least one constrained automation delivers on a cadence to a known path.
6. **Level 5, Self-maintaining.** The Weekly OS Audit runs every Sunday and you action its proposals. The OS now improves itself.

Most of the value arrives at Level 2. Most of the durability arrives at Level 5.

---

## The one-week plan

You do not need a quarter for this. One layer at a time, one week. (A focused afternoon gets you through the first three.)

- **Mon.** Run `build-context`. Write your profile, strategy, and product-area files. Stand up the router. End with the agent drafting a message in your voice.
- **Tue.** Run `map-connections`. Map your three or four real tools.
- **Wed.** Run `forge-skill` on the prompt you type most, then twice more for your next two repeated prompts.
- **Thu.** Run `schedule-automation` for one recurring deliverable with a hard constraint.
- **Fri.** Run `seed-memory`. Approve three starter memories. Wire the always-read-memory rule into the router.
- **Sun.** Run `weekly-os-audit` to create and schedule the loop. Let it run its first Sunday cycle.

By the end of week one you are at Level 5: a context-loaded, connected, skilled, automated, memory-backed AI OS that audits itself every week. From there, action the audit each Sunday and the OS keeps improving on its own.
