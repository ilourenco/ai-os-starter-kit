# CLAUDE.md — My AI OS Router

**Read this file first. It is the index of my whole AI OS.**

This file is the spine. It is read at the start of every interaction, it indexes every layer below, and each layer registers itself here. Keep it under 80 lines.

## Global rules

These apply to everything you produce for me. Replace with your own once `build-context` runs.

1. Lead with the conclusion, then the detail.
2. Be concrete. Favour examples over adjectives.
3. No dashes used as punctuation. Use commas, periods, or parentheses.
4. Write in my voice (see `context/`), never generic AI prose.
5. If you are unsure, ask one sharp question rather than guessing.
6. [Your recurring correction goes here, captured by build-context.]

## Context

The files you read to know who I am. Keep each under 500 words.

- `context/profile.md` — who I am, how I write, my principles. (Renamed to `context/pm.md` for product managers.)
- `context/strategy.md` — this quarter's priorities, what is locked, what is open.
- `context/product-area.md` — my domain, ICP, and the metric I own. (Product managers only.)

## Connections

The tools you can reach. Mapped by `map-connections`.

- `connections.md` — the few tools I actually use, with triggers. Reach for a tool only when its trigger matches.

## Skills

Reusable patterns you invoke by trigger. Registered by `forge-skill`.

| Skill | Purpose | When to use | Created |
|---|---|---|---|
| (your skills get registered here) | | | |

## Automations

Scheduled prompts that run without me. Indexed by `schedule-automation`.

- `automations/README.md` — the index of everything scheduled, with cadence and constraint.

## Memory

Typed, approved facts that persist between conversations. Seeded by `seed-memory`.

1. At the start of every conversation, read `./MEMORY.md` before responding.
2. If I correct you on the same thing twice, propose a FEEDBACK memory. Never save a memory I have not approved.
3. Flag any PROJECT memory past its expiry date for review.
