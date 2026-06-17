---
name: seed-memory
description: Builds Layer 5 (Memory) of the user's Personal AI OS. Use when the user says "seed my memory", "set up memory", "seed-memory", or asks the agent to remember facts across conversations. Proposes typed starter memories for approval and wires the always-read-memory rule into the router.
creates:
  - MEMORY.md (typed, approved entries)
  - updates CLAUDE.md (## Memory section)
---

# Seed Memory (Layer 5)

You are building Layer 5. Memory is typed, approved facts that persist between conversations. The discipline that makes it safe: nothing is saved without the user's yes.

## The four types

- **USER**: durable facts about the user (role, company, how they work).
- **FEEDBACK**: a correction the user has given, with the why.
- **PROJECT**: a time-bound fact about current work. Requires an expiry date.
- **REFERENCE**: a pointer to an external resource (dashboard, doc, ticket).

## Propose starter memories

Read `context/` if it exists, to ground the proposals in real facts. Then propose **three** starter memories: one USER, one FEEDBACK, one REFERENCE. Each on one line, each with a **why** and **today's date**.

Present all three and ask the user to **approve, edit, or reject each one**. Save only what they approve. If the user wants a PROJECT memory, **require an expiry date** before saving it.

## Write the file

Save approved entries to **`MEMORY.md`**, each typed and dated. Use this row shape:

```
- [USER] <fact> — why: <reason> — saved: <date>
- [FEEDBACK] <correction> — why: <reason> — saved: <date>
- [PROJECT] <fact> — why: <reason> — saved: <date> — expires: <date>
- [REFERENCE] <resource> — why: <reason> — saved: <date>
```

## Wire the router

Update **`CLAUDE.md`** under the `## Memory` header with three rules:

1. **Load rule**: "At the start of every conversation, read ./MEMORY.md before responding."
2. **Capture rule**: "If I correct you on the same thing twice, propose a FEEDBACK memory. Never save a memory I have not approved."
3. **Maintenance rule**: "Flag any PROJECT memory past its expiry date for review."
