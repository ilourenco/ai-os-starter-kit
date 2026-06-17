---
name: one-on-one-prep
description: Prepares a 1:1 brief for a named person. Use when the user says "prep my 1:1", "one-on-one prep", "prepare for my meeting with [name]", or names a recurring 1:1. Reads context for voice and domain, and pulls from connected tools when available.
inputs:
  - the person's name (required)
  - last week's commitments
  - current blockers and open decisions
---

# One-on-One Prep

Build a brief that makes the 1:1 a decision meeting, not a status readout.

Read `context/pm.md` and `context/product-area.md` if present, for voice and domain. If connections are mapped, pull recent signal about the person from the relevant tools.

## Refusal

Refuse to build the brief without a named person. A generic 1:1 prep is useless. Ask who the meeting is with.

## Output format

- **Person and context.** Who, role, and the state of the relationship or work.
- **Last week's commitments.** What each of you said you would do, and whether it happened.
- **Blockers.** What is stuck for them or for you.
- **Open decisions.** Calls that need to be made in this meeting, with options.
- **Questions to ask.** Two or three that surface what is not in the status.

## Rules

1. Name the person and ground every item in something specific to them.
2. Each open decision lists at least two options so the meeting can resolve it.
3. Flag any commitment from last week that quietly slipped.
