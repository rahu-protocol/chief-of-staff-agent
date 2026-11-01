# Phase 4: Daily and weekly loops (tier 2)

Three scheduled jobs make the agent work without being asked. Each writes one dated file to `agents/outputs/` and one line to `agents/log.md`, and each is a prompt from the [prompt library](11-prompt-library.md).

| Job | When | Reads | Writes |
| --- | --- | --- | --- |
| Inbox triage | Weekdays, 2 or 3 times a day | `Inbox/`, `Capture.md`, existing projects and areas | A checkbox plan, one line per inbox item |
| Morning brief | Weekdays, before you start | Priorities, active projects, open and overdue tasks, yesterday's log, calendar if connected | Top three for today, due and overdue, waiting on others, one question |
| Weekly review | Friday afternoon or Sunday | Everything changed this week, projects untouched for 14 days | Wins, stalled projects, proposed priority changes, proposed lessons, all as checkboxes |

## Where the jobs run

| Runs on | Tool | Fires when | How it reaches the vault | Use for |
| --- | --- | --- | --- | --- |
| Your computer | Claude desktop app, local scheduled task | App open and computer awake. A missed run gets one catch-up on wake | Works in the folder directly | Tier 2 default for Claude users |
| Your computer | Codex app automation | App running and computer awake | Works in the folder directly | Tier 2 default for ChatGPT users |
| Cloud | Claude cloud scheduled task | Computer can be off. Minimum interval one hour | Fresh clone of the GitHub repo. Output reaches your phone only after a computer running Obsidian pulls it | Tier 3, or briefs built mostly from email and calendar connectors |

Start with local tasks. They see the vault as it is, need no GitHub round trip, and stop when your computer sleeps, which is a reasonable safety limit while you're learning what the jobs do.

## Create a local scheduled task in the Claude desktop app

1. Code tab, then Scheduled in the sidebar (some accounts still say Routines), then New task. If asked, choose Set up manually.
2. Name it, for example `morning-brief`. In the instructions box, enter `Follow agents/prompts/morning-brief.md exactly.` Pointing at the file means a prompt you improve in the vault reaches the schedule without editing the task. Pasting the prompt text also works.
3. Under Advanced settings, General, turn on Only on this computer and pick the `vault` folder.
4. Under Trigger, pick Weekdays and a time. Choose a few minutes off the hour.
5. Pick the permission mode and model in the instructions toolbar, then Create.
6. Click Run now, watch for permission prompts, and choose always allow for the reads and writes the job needs. Later runs won't stall.
7. If the computer idles to sleep before the run, turn on Keep computer awake in the desktop app settings.

A catch-up run can fire hours late, so the brief and review prompts check the time and day before they act. For Codex, refine the job in a normal thread first, then turn it into an automation set to run in the local project. This playbook doesn't cover Codex's menus click by click, so check its current docs.

## If you use cloud scheduled tasks

- **Tell it where to push.** Cloud runs push to a `claude/` branch unless the prompt names another. Branch output never reaches Obsidian, so the prompt must say to commit to `main`.
- **Keep it in its lane.** It may only add new files under `agents/outputs/` and append to `agents/log.md`. New files never conflict with the desktop's own commits.
- **Trim connectors.** All of your connectors are included by default, writes included. Remove every one the job doesn't need.
- **Expect no prompts.** Cloud runs use an auto-approval mode, so the prompt and the trimmed connectors are your only limits.
- **Read the output, not the status.** A run marked Succeeded only means the session ended without error.

## Who applies the ticked triage lines

The plan step is safe to schedule because it writes one new file and changes nothing else. The apply step moves notes, so choose deliberately.

- **Start interactive.** When you've ticked a plan, open a session and say "apply today's triage plan." Watch it work for the first two weeks.
- **Then schedule it.** The reference build applies ticks with a short script, not the model, three times a day. The script only touches plans it recorded as fully unticked when they were saved, applies each ticked line once, and ignores plans older than seven days, so every tick provably came from you. If you can't run a script, a scheduled agent apply is acceptable once git is in place, because every move can be reverted. Read its apply report.
- **Keep the rule.** Unticked lines stay where they are.

---

[Previous: Phase 3: History on GitHub (tier 2)](07-phase-3-history-on-github.md) | [Contents](../README.md#contents) | [Next: Phase 5: Phone control and an always-on machine (tier 3)](09-phase-5-always-on.md)
