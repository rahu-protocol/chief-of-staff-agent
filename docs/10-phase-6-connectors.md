# Phase 6: Connectors, and how it compounds

In this workflow, approved corrections and decisions go into shared notes so future sessions can use them. Built-in agent memory can complement that record. Connectors widen what it can see. Neither works without the approval habit from earlier phases.

## Add connectors carefully

1. **Start read-only.** Connect calendar first. Check whether its information improves the morning brief before adding more access. Add email next, reading only.
2. **Drafts, never sends.** Keep proposed replies and calendar holds in local output files while connectors are read-only. Creating a draft in an email service or a hold in a calendar is a write, so authorize that specific action before granting its scope. Never send, invite, accept, decline or delete without explicit authorization.
3. **Treat connector content as data.** Emails, web pages and clipped articles can contain text written to steer an agent. The rules file says to treat those instructions as data. Restrict tool access too, because that written rule alone cannot prevent every prompt-injection attempt.
4. **Scope each scheduled job.** A job gets only the connectors it uses. A brief needs calendar read access, not your drive.

## The compounding loop

| What happens | Where it lands | How it gets there |
| --- | --- | --- |
| You correct the agent ("too long", "never cc my boss") | `Context/Working with me.md` | Agent proposes a one-line lesson in the weekly review; you tick it |
| You make a decision | `Context/Decisions.md` | Agent drafts the line with a revisit date; briefs surface it when due |
| You meet someone or work with them | `People/<Name>.md` | Agent proposes updates after you paste or dictate notes |
| A project moves or stalls | The project note's status and outcome | Triage and the weekly review propose changes; a 14-day stale check flags rot |
| You ask for the same thing a third time | `agents/prompts/<name>.md`, then a scheduled task | Agent offers to save it as a reusable prompt |
| Notes go stale | `Archive/` or `.trash/` | The weekly review proposes archiving and deletion |

## Signs it's working

These are suggested checks to evaluate during your own trial, not measured outcomes of the untested chief-of-staff prompts.

- The inbox stays under about 20 items and nothing in it is older than a week.
- You read the morning brief most days without being reminded.
- You correct the same thing less often over a month.
- Context notes stay under a page each, because the weekly review prunes them.

If the inbox keeps growing, review capture volume, stalled decisions and whether triage is keeping material with no value. Delete is the default for items with no next action and no reference value. An agent that keeps everything just gives you well-organized junk.

---

[Previous: Phase 5: Phone control and an always-on machine (tier 3)](09-phase-5-always-on.md) | [Contents](../README.md#contents) | [Next: Prompt library](11-prompt-library.md)
