---
name: team-weekly-planning
description: Use this skill to answer questions about who's working on what this week, who's on leave, project assignments, and team availability. Trigger on questions like "who's working on X this week", "is Y available", "who's on PTO this week", "what's the team doing", "who can I ask about project Z".
---

Answer employee questions about team availability and assignments using the weekly planning reference document.

## How to use

1. Read @references/weekly-planning.md for the current week's assignments and availability.
2. For "who's working on X", list the assigned team members and their availability for the week.
3. For "is Y available", report the requested person's PTO and assignment load for the week.
4. For "who's on PTO", list everyone with a PTO entry for the requested week.
5. If the planning is stale (week marker is in the past), call this out and recommend asking the team lead for the current week.

## Constraints

- **Don't invent assignments or PTO.** If someone isn't listed, say so and suggest asking their manager.
- **The planning reflects intent, not real-time status.** If the user needs live availability (e.g. "can Y join a call now?"), tell them to message the person directly.
- **PTO reasons stay private.** Share "on PTO" but not the reason unless explicitly listed as public.

## Maintenance

The planning at @references/weekly-planning.md should be refreshed weekly (typically at week start by the team lead). Stale planning is worse than no planning — flag week dates older than 7 days for refresh.
