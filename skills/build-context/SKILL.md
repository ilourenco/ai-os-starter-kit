---
name: build-context
description: Builds the Context half of Layer 1 (Context) of the user's Personal AI OS, the organizational half. Use when the user says "build my context", "build-context", "add my org context", or after running build-identity. Reads CLAUDE.md first, interviews the user one question at a time, and writes their context file. Run build-identity first.
creates:
  - context/context.md
---

# Build Context (Layer 1, part 2)

You are building the organizational half of the user's Context layer: their company, their domain, and what is decided. This is the second of the two Context parts. Identity (the personal half) comes first.

Read `CLAUDE.md` first. If it does not exist, tell the user to run `build-identity` first and stop, because the router and `context/identity.md` must exist before this skill runs.

Interview the user **one question at a time**. Wait for each answer before asking the next. Use a multiple-choice question whenever the options are knowable.

## Interview sequence

Ask these in order, one at a time.

1. **Company and stage.** What the company is and where it is in its life (pre-seed, seed, Series A-B, growth, public, agency).
2. **Area I own.** The surface they own, in one sentence.
3. **ICP.** Their ideal customer profile, in one sentence.
4. **Top metric.** The single metric they are accountable for, with its current value.
5. **This quarter.** The top 3 priorities, and explicitly the one thing they said no to.
6. **Locked and open.** What is decided (do not relitigate) and what is still in flight. Max 5 each.

## Then write the file

Apply the writing rules: no dashes used as punctuation, no "X, not Y" scaffolding, no "most teams" generalizations, no reveal preambles. Be concrete. Lead with the conclusion.

1. **`context/context.md`.** Under 400 words. Sections: Company and stage, Area I own, ICP, Top metric, This quarter (priorities and the one no), Locked, Open.
2. **`CLAUDE.md`.** Under `## Context`, point to `context/context.md` as the organizational half, alongside `context/identity.md`. Keep the note that Context has two parts.

## Prove it

Show the user `context/context.md` and the updated `## Context` section. Then ask the agent a question that needs org context (for example, "given what is locked, what should I not propose?") and confirm it answers from the file without being told.
