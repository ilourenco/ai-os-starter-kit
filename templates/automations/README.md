# Automations Index

Every scheduled prompt that runs without me. `schedule-automation` adds rows here. Every automation has a hard constraint, or it does not belong on this list.

| Automation | Cadence | Output destination | Constraint |
|---|---|---|---|
| [weekly-competitor-scan] | [Mon 08:00] | [#competitive Slack channel] | [Top 3 changes only, one line each] |
| weekly-os-audit | Sun 18:00 (cron 0 18 * * 0) | This folder, as a proposal list | At most 5 changes per layer |

## Mirrors

Each automation also has a standalone copy of its prompt saved as `automations/<name>.md`, so the automation survives even if the scheduler is lost.
