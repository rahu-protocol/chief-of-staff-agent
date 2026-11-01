# Vault rules

Shared rules for all agents are in the AGENTS.md one folder up. Read them first.

## Before chief-of-staff work

Read Context/Me.md, Context/Priorities.md and Context/Working with me.md. Read a person's note in People/ before drafting anything to or about them.

## Writing

- Notes are Markdown with Obsidian syntax: [[wikilinks]], embeds, and YAML properties at the top.
- Never delete, rename or move an existing note without asking. Renames break links. The one exception is a plan the person approved.
- Agents write new material only under agents/, except when applying an approved plan:
  - agents/outputs/YYYY-MM-DD-<slug>.md for job results and plans.
  - agents/log.md for one line per job.
- Never edit Context/ directly. Propose changes as a plan. The one exception: append an approved lesson under Lessons in Context/Working with me.md.
- Do not edit .obsidian/ (app settings and plugins).
- Changes sync to phone and tablet within a minute and commit to GitHub every 10 minutes. Mistakes spread fast.

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
3. Write the plan to agents/outputs/YYYY-MM-DD-inbox-triage.md, one unticked checkbox per item, five fields separated by " | ":
   - [ ] SOURCE | ACTION | DESTINATION | PROPERTIES | REASON
   - SOURCE: Inbox/<file>, or Capture: <exact line text>. Match lines by exact text, never by line number.
   - ACTION: task, note, idea, project, area, merge or delete.
   - DESTINATION: Tasks/<Name>.md, Notes/<Name>.md, Projects/<Name>.md, Areas/<Name>.md, an existing note for merge, or - for delete.
   - PROPERTIES: {type: task, status: active, project: "[[Project note]]"}; {} for merge and delete.
   - REASON: short free text.
   Change nothing else in this step.
4. Stop. The person ticks the items they approve, on any device.
5. Apply only ticked items: create or move notes, set properties, add links, move approved deletes to .trash/, and remove processed lines from Capture.md. Unticked items stay where they are. Skip any line that can't be applied and list it in the apply report.
6. A new plan covers the whole inbox, so the newest plan is the complete list.
7. Append one line to agents/log.md for the plan and one for the apply step.

## Lessons

When I correct you, end your reply by proposing a one-line rule. Append it under Lessons in Context/Working with me.md only after I approve it.
