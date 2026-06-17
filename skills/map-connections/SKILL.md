---
name: map-connections
description: Builds Layer 2 (Connections) of the user's Personal AI OS. Use when the user says "map my connections", "set up my tools", "map-connections", or asks the agent to learn which tools it can use. Enumerates installed connectors, interviews the user about the few they actually use, and writes connections.md.
creates:
  - connections.md
  - updates CLAUDE.md (## Connections section)
---

# Map Connections (Layer 2)

You are building Layer 2. The goal is a short, honest map of the tools the user actually works in, so the agent reaches for the right one instead of guessing.

## First, enumerate (do not guess)

Call the connector-listing tool to list the connectors actually installed for this user. Do not invent or assume connectors. Show the user the real list.

If no connector-listing tool is available, ask the user to name the connectors they have authorized, and proceed from there.

## Then interview

Three used beats twelve connected. Ask the user, one question at a time:

1. **Which 3 to 4 connectors do you really use?** Present the enumerated list as multiple choice. Push back gently if they pick more than four.
2. For **each** chosen connector, ask three short questions:
   - What do you use it for?
   - When should the agent reach for it (the trigger)?
   - One cross-tool question it helps answer (for example: "which leads from the Notion pipeline went quiet in Slack this week?").

## Then write the file

Write **`connections.md`** as a table with one row per connection and these columns: **Tool**, **Purpose**, **When to use**, **Example query**. Keep it tight. Only the tools the user named.

Add a short line at the top: "The agent maps to these tools only. If a task needs a tool not listed here, ask before assuming it is connected."

## Then register it

Update **`CLAUDE.md`** under the `## Connections` header with a single pointer line: "My connections are mapped in ./connections.md. Reach for a tool only when its trigger matches." Do not paste the whole table into the router. The router points, the file holds detail.
