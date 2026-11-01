# Vault rules

Shared rules for all agents are in the AGENTS.md one folder up. Read them first.

## Before chief-of-staff work

Read Context/Me.md, Context/Priorities.md and Context/Working with me.md. Read a person's note in People/ before drafting anything to or about them.

## Writing

- Notes are Markdown with Obsidian syntax: [[wikilinks]], embeds, and YAML properties at the top.
- Never delete, rename or move an existing note without asking. Renames break links. The one exception is a plan the person approved.
- Agents write new material only under agents/, except when applying an approved plan:
  - agents/outputs/YYYY-MM-DD-HHMMSS-<run-id>-<slug>.md for job results and plans.
  - agents/log.md for one line per job.
- Change Context/ only while applying the exact entries a person approved in a named plan, or when appending a lesson whose exact wording they approved. Never save an inferred preference as an approved fact.
- Do not edit .obsidian/ (app settings and plugins).
- Sync and Git timing depend on configuration and device availability. Git records commits, not every edit. Check sync and history before relying on recovery.
- Run one writer at a time in this vault. Use a new run ID and unused output path for every run. These instructions do not create a technical lock.

## Folders

- Inbox/: everything new lands here. Inbox/Capture.md is the capture log, one line per capture.
- Projects/: one note per project. A project has an outcome and an end.
- Areas/: ongoing responsibilities with no end date.
- Tasks/: one note per task.
- Notes/: reference material worth keeping.
- People/: one note per person I work with.
- Context/: who I am and what matters now.
- Archive/: projects and notes that are done or dropped.
- Attachments/: images and files.
- agents/: outputs, saved prompts, and the job log.

## Properties

Every note outside Inbox/, Context/ and agents/ starts with two properties. Use these values exactly; the views filter on them.

- type: task | project | area | note | idea | person
- status: active | waiting | done | dropped

- Task: add project: "[[Project note]]" or area: "[[Area note]]". Add due: YYYY-MM-DD only for a real date.
- Project: add outcome: with one line saying what done looks like.
- Person: add role: and org: when known.
- Every task links to a project or area. Never invent links to fill the graph.

## Inbox triage

1. Read every file in Inbox/ and every line in Inbox/Capture.md. A leading word (task, idea, ref, or a project name) says what the person meant. A [[link]] in an item names its project.
2. Propose exactly one action per item: new task, new note, new project, merge into an existing note, or delete. Default to delete when an item has no next action and no reference value.
3. Write the plan to a new agents/outputs/YYYY-MM-DD-HHMMSS-<run-id>-inbox-triage.md, one unticked checkbox per item, five fields separated by " | ":
   - [ ] SOURCE | ACTION | DESTINATION | PROPERTIES | REASON
   - SOURCE: Inbox/<file>, or Capture: <exact line text>. Match lines by exact text, never by line number.
   - ACTION: task, note, idea, project, area, merge or delete.
   - DESTINATION: Tasks/<Name>.md, Notes/<Name>.md, Projects/<Name>.md, Areas/<Name>.md, an existing note for merge, or - for delete.
   - PROPERTIES: {type: task, status: active, project: "[[Project note]]"}; {} for merge and delete.
   - REASON: short free text.
   Change nothing else in this step.
4. Stop. The person reviews and ticks selected items, then names this exact plan path in an interactive apply request. Do not infer approval from a pre-ticked file alone.
5. In that interactive session, validate selected entries and compare previous apply reports before acting. Skip previously completed actions. If the source changed, an identical capture appears more than once, or a prior run ended without a reliable report, stop that item and ask. Apply only confirmed ticked entries: create or move notes, set properties, add links, move approved deletes to .trash/, and remove processed lines from Capture.md by exact text. Preserve unticked entries.
6. Keep older plans. Do not silently switch to the newest plan. Every apply report names its exact source plan, the selected entry text, each completed action and each skipped or uncertain item.
7. Append one line to agents/log.md for the plan and one for the apply step.

## Applying other approved plans

Onboarding, meetings, project kickoffs and reviews use the same interactive procedure: the person names the exact plan, confirms selected entries and their proposed content, and the agent checks prior apply reports and current files before acting. Apply only that content, including approved Context/ changes. Save a fresh agents/outputs/YYYY-MM-DD-HHMMSS-<run-id>-plan-applied.md report and append to the log. Ask about changed or ambiguous sources. Do not schedule application with these prompts alone.

## Lessons

When I correct you, end your reply by proposing a one-line rule. Append it under Lessons in Context/Working with me.md only after I approve it.
