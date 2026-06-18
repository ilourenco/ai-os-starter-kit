---
name: build-identity
description: Builds the Identity half of Layer 1 (Context) of the user's Personal AI OS. Use when the user says "build my identity", "set up my AI OS", "build-identity", "build my context", or starts the kit for the first time. Interviews the user one question at a time and writes their identity file and the router. Context has two parts; this is the first. Run build-context next.
creates:
  - context/identity.md
  - CLAUDE.md (the router)
---

# Build Identity (Layer 1, part 1)

You are building the personal half of the user's Context layer: who they are, and the rules their agent must always enforce. Context has two parts, identity (personal) and context (organizational). This skill builds identity and the router. `build-context` builds the organizational half next.

Interview the user **one question at a time**. Wait for each answer before asking the next. Use a multiple-choice question whenever the options are knowable. Never ask the user for adjectives to describe their own voice. Capture voice from a writing sample instead.

## Interview sequence

Ask these in order, one at a time.

1. **Role and seniority.** Offer choices: founder / product manager / product leader / engineer / marketer / RevOps / operations / other. Then ask company stage: pre-seed / seed / Series A-B / growth / public / agency.
2. **Voice.** Ask the user to paste 3 to 5 lines they wrote recently (a Slack post, an email, a doc). Tell them not to clean it up. Capture cadence, sentence length, and habits from this. Do not ask them to describe their style.
3. **Non-negotiables.** Ask for exactly three. The lines they will not cross.
4. **Banned phrases.** Ask for words or phrases the agent must never use in their voice.
5. **Rules the agent must always enforce.** Ask for the rules that should hold on every output. Include the one correction they keep giving their AI.

## Then write the files

Apply the writing rules: no dashes used as punctuation, no "X, not Y" scaffolding, no "most teams" generalizations, no reveal preambles. Be concrete. Lead with the conclusion.

1. **`context/identity.md`.** Under 500 words, in the user's voice. Sections: Role, Voice (with one or two captured habits from the sample), Principles, Non-negotiables (exactly three), Banned phrases, Rules my agent enforces.
2. **`CLAUDE.md`** (the router). Under 80 lines. It must:
   - Open with the top rule: "Read this file first. It is the index of my whole AI OS."
   - Point at `context/identity.md` under `## Context`, and note that Context has two parts: identity (now) and context (next, built by `build-context`).
   - Carry 5 to 8 global rules written in the user's voice, including the recurring correction from question 5.
   - Contain the five section headers exactly: `## Context`, `## Connections`, `## Skills`, `## Automations`, `## Memory`. Leave the later sections as short placeholders that the other builder skills will fill.

## Prove it

End the session by drafting a short message in the user's voice (a two-line Slack update or a status note) without being told to. This proves the identity is loaded and readable. Ask the user if it sounds like them, and tune `context/identity.md` if it does not. Then tell them the next step is `build-context`.
