---
name: forge-skill
description: Builds Layer 3 (Skills) of the user's Personal AI OS. Use when the user says "forge a skill", "make a new skill", "forge-skill", "turn this into a skill", or describes a prompt they keep retyping. Captures one repeated task as a reusable SKILL.md and registers it in the router.
creates:
  - skills/<name>/SKILL.md
  - updates CLAUDE.md (## Skills section)
---

# Forge Skill (Layer 3)

You are turning a repeated prompt into a reusable skill. The rule of thumb: write the skill the third time the user types the same prompt.

## First, check what exists

List the folders under `skills/` so you do not rebuild something that already exists. If a close match exists, offer to extend it instead of creating a duplicate.

## Then find the task

Ask the user, one question at a time:

1. **What task have you given an AI three or more times?** If the user is new and has no repeated task yet, offer a canonical product management skill to build (for example: a standup summary, a meeting-notes-to-actions converter, a feature one-pager).
2. **Trigger words.** What phrases should invoke this skill? Capture 3 to 5.
3. **Inputs.** What does the skill need from the user every time (a source, a name, a metric)?
4. **Output format.** What should the result look like (sections, length, tone)?

## Then write the skill

Write **`skills/<name>/SKILL.md`** with:

- **YAML frontmatter**: `name` (kebab-case), `description` in the third person with the trigger phrases woven in, and `inputs` listing what it needs.
- **An instructions body** written verb-first, as directives for the agent.
- **Exactly three rules.** One of the three must be a refusal (a condition under which the skill stops and asks rather than guessing). Example: "Refuse to draft without a named owner."

Keep the body opinionated and short. A skill that tries to do everything does nothing well.

## Then register it

Update **`CLAUDE.md`** under the `## Skills` header by adding a table row: **name**, **purpose**, **when to use**, and **today's date** (created). A skill not in the router is invisible to the agent. Registration is the step people skip, so do not skip it.
