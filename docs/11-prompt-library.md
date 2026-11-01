# Prompt library

Nine prompts cover the daily work. Each one lives as a file in the starter vault's [`agents/prompts/`](../starter-kit/ai-workspace/vault/agents/prompts/) folder, so every agent and every scheduled task uses the same wording, and an improvement made once reaches all of them.

To run one, start a session inside the vault and type `Follow agents/prompts/<file>.md`, or paste the prompt text. Scheduled tasks take the same one-line instruction. Text in angle brackets, such as `<Name>`, is yours to replace. `YYYY-MM-DD` and `HHMMSS` use the local run date and time. `<run-id>` is a fresh identifier generated for this run.

| Prompt | What it does | When to run it |
| --- | --- | --- |
| [Onboarding interview](../starter-kit/ai-workspace/vault/agents/prompts/onboarding-interview.md) | Interviews you for about 20 minutes, then proposes your context, project, area and people notes as a plan. | Once, in an interactive session, after the rules files are in place. |
| [Inbox triage: plan](../starter-kit/ai-workspace/vault/agents/prompts/inbox-triage-plan.md) | Writes a checkbox plan with one proposed action per inbox item. Updates the log but changes no source notes. | Scheduled, weekdays, initially once a day. Increase only after checking overlap and usefulness. |
| [Inbox triage: apply](../starter-kit/ai-workspace/vault/agents/prompts/inbox-triage-apply.md) | Applies only the ticked lines of the latest plan and writes a report. | Interactive at first, after you tick lines in a plan. |
| [Morning brief](../starter-kit/ai-workspace/vault/agents/prompts/morning-brief.md) | Top three for today, due and overdue, waiting on others, meeting prep, decisions due, one question. | Scheduled, weekdays, before you start work. |
| [Weekly review](../starter-kit/ai-workspace/vault/agents/prompts/weekly-review.md) | Wins, stalled projects, and proposed changes to priorities, lessons and context notes, all as checkboxes. | Scheduled, Friday afternoon or the weekend. |
| [Capture a lesson](../starter-kit/ai-workspace/vault/agents/prompts/capture-a-lesson.md) | Turns a correction into a one-line rule and saves it after you approve. | Interactive, right after you correct the agent. |
| [Meeting notes to actions](../starter-kit/ai-workspace/vault/agents/prompts/meeting-notes-to-actions.md) | Proposes tasks, waiting items, people-note updates and decisions from your notes. | Interactive, after a meeting. |
| [Project kickoff](../starter-kit/ai-workspace/vault/agents/prompts/project-kickoff.md) | Asks up to five questions, then proposes a project note and its first tasks. | Interactive, when something new starts. |
| [Draft a reply](../starter-kit/ai-workspace/vault/agents/prompts/draft-a-reply.md) | Drafts a reply using the sender's people note and your writing rules. Never sends. | Interactive. |

The brief and review prompts check the day and time before acting, because some schedulers catch up after sleep. Triage has its own apply prompt. For onboarding, project and review plans, name the exact plan and use the approved-plan procedure in the vault rules. For each run, use a unique output filename: YYYY-MM-DD-HHMMSS-<run-id>-<slug>.md. Generate a fresh run ID, check the path is unused, and never replace an existing output. Run one writer at a time. Apply changes only in an interactive session after the person names the exact plan and confirms the selected entries. Record the source plan and applied items in a new report. The prompts describe behavior; they do not implement file locks, authenticated approvals or an unattended application engine.

---

[Previous: Phase 6: Connectors, and how it compounds](10-phase-6-connectors.md) | [Contents](../README.md#contents) | [Next: Failure modes and guardrails](12-failure-modes.md)
