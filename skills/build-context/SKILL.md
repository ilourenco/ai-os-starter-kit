---
name: build-context
description: Builds Layer 1 (Context) of the user's Personal AI OS. Use when the user says "build my context", "set up my AI OS", "build-context", "create my profile", or starts the kit for the first time. Interviews the user one question at a time and writes their profile, strategy, product-area, and router files.
creates:
  - context/profile.md (renamed to context/pm.md if the user is a product manager)
  - context/strategy.md
  - context/product-area.md (product managers only)
  - CLAUDE.md (the router)
---

# Build Context (Layer 1)

You are building the foundation of the user's Personal AI OS. Context is the set of files the agent reads at the start of every interaction. Get this right and every later layer compounds.

Interview the user **one question at a time**. Wait for each answer before asking the next. Use a multiple-choice question whenever the options are knowable. Never ask the user for adjectives to describe their own voice. Capture voice from a writing sample instead.

## Interview sequence

Ask these in order, one at a time.

1. **Role and company stage.** Offer choices: founder / product manager / product leader / engineer / marketer / RevOps / operations / other. Then ask company stage: pre-seed / seed / Series A-B / growth / public / agency.
2. **Writing sample.** Ask the user to paste 2 to 3 paragraphs they wrote recently (a Slack post, an email, a doc). Tell them not to clean it up. Capture cadence, sentence length, and habits from this. Do not ask them to describe their style.
3. **Leadership principles.** Ask for 3 to 5 principles they actually operate by.
4. **Non-negotiables.** Ask for exactly three.
5. **Banned phrases.** Ask for words or phrases the agent must never use in their voice.
6. **AI dos and don'ts.** Ask for three things the agent should always do and three it should never do.
7. **This quarter's priorities.** Ask for the top 3, and explicitly ask what they said no to this quarter.
8. **Domain.** Ask four short questions: ICP in one sentence; the top metric they own; what is locked (decided, do not relitigate); what is still open.
9. **Tools.** Ask which tools they use most (this seeds Layer 2 later).
10. **The recurring correction.** Ask: "What is the one correction you keep giving your AI?" This becomes a top global rule in the router.

## Then write the files

Apply the writing rules: no dashes used as punctuation, no "X, not Y" scaffolding, no "most teams" generalizations, no reveal preambles. Be concrete. Lead with the conclusion.

1. **`context/profile.md`** (rename to **`context/pm.md`** if the user is a product manager). Under 500 words. Sections: who I am, how I write (with one or two captured habits from the sample), leadership principles, non-negotiables, banned phrases, AI dos and don'ts, the recurring correction.
2. **`context/strategy.md`.** Under 200 words. This quarter's top 3 priorities, what they said no to, what is locked, what is still open.
3. **`context/product-area.md`** (product managers only). ICP in one sentence, the top metric owned, the product area, what is locked, what is still open.
4. **`CLAUDE.md`** (the router). Under 80 lines. It must:
   - Open with the top rule: "Read this file first. It is the index of my whole AI OS."
   - Point at the context files by path.
   - Carry 5 to 8 global rules written in the user's voice, including the recurring correction from question 10.
   - Contain the five section headers exactly: `## Context`, `## Connections`, `## Skills`, `## Automations`, `## Memory`. Leave the later sections as short placeholders that the other builder skills will fill.

## Prove it

End the session by drafting a short message in the user's voice (a two-line Slack update or a status note) without being told to. This proves the context is loaded and readable. Ask the user if it sounds like them, and tune one file if it does not.
