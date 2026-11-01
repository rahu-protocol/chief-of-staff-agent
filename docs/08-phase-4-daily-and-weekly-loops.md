# Phase 4: Daily and weekly loops (tier 2)

Run each job interactively before scheduling it. Every run uses a fresh output name, `YYYY-MM-DD-HHMMSS-<run-id>-<slug>.md`, and records its result in `agents/log.md`. A run ID distinguishes repeated jobs in the same second. Check that the path does not exist before writing. Never replace an earlier plan or output.

| Job | When | Reads | Writes |
| --- | --- | --- | --- |
| Inbox triage plan | Weekdays, initially once a day | Inbox, capture log, projects and areas | One unticked plan, with the exact source for each action |
| Morning brief | Weekdays, before work | Priorities, tasks, decisions and available calendar data | A linked brief with missing information stated |
| Weekly review | Friday afternoon or weekend | Recent changes and active work | Proposed changes as unticked checkboxes |

Run one writer at a time, including manual sessions, schedules and Git updates. Do not edit a plan from two devices while applying it. More frequent triage can come later if it stays useful and jobs do not overlap.

## Where the jobs run

| Runs on | Tool | Requirements | File access | Use for |
| --- | --- | --- | --- | --- |
| Your computer | Claude Desktop local scheduled task | App running and computer awake | Selected local folder | Start here for Claude users |
| Your computer | Codex local project schedule | Computer on and desktop app running | Project directory or isolated worktree, as selected | Select the actual vault copy, or review and merge worktree output |
| Cloud | Repository-based Claude scheduled task | Configured repository, environment and tools | Repository copy, not Obsidian Sync | Optional after testing the review and sync path |

These are the paths covered by this build. Current products also offer other cloud schedules. Check the job's execution location, account access and tools instead of assuming it sees your local vault.

## Create a local scheduled task in the Claude desktop app

1. **Open the schedule form.** In Claude Desktop's Code tab, open Scheduled, then New task. Some versions show Routines. If offered, choose Set up manually.
2. **Choose local execution.** Select Local or turn on Only on this computer, depending on the form. If that switch is at the top, turn it on before filling the rest of the form. Select the vault folder.
3. **Name the job and point to its prompt.** For example, name it morning-brief and enter Follow agents/prompts/morning-brief.md exactly. A saved file keeps later prompt edits in one place.
4. **Set the schedule.** Choose weekdays and a local time. Separate jobs so their expected run times do not overlap.
5. **Review the permission mode and model.** Grant only the file and tool access this job needs. Rules in a prompt do not restrict a tool technically.
6. **Run it while watching.** Use Run now, inspect the output and log, and review any permission request. Save only narrow approvals you understand. Some tools require interaction on every call, so a watched success does not guarantee unattended runs will finish.
7. **Check sleep and missed-run behavior.** Local Claude schedules need the app open and computer awake. Its documented catch-up behavior can produce a late run, so inspect run history and keep the brief and review time checks.

For Codex, test the prompt in a normal chat first, then create a schedule for the local project. Confirm whether it runs in the project or a worktree. An unattended run may fail or wait when permissions are insufficient. See the current [scheduled task guide](https://learn.chatgpt.com/docs/automations).

## If you use cloud scheduled tasks

- **Review the output branch.** Repository-based cloud jobs can write to a separate branch. Review and merge intended changes into the branch the desktop pulls. Direct writes to that branch require an explicit decision and coordinated Git access.
- **Coordinate every writer.** Unique output files reduce overlap, but agents/log.md, notes and branch updates remain shared. Start with one writer in the vault. A cloud run may write its own report, with the desktop writer adding the log entry after review.
- **Trim connectors.** Claude's documented cloud task form includes connected MCP tools by default, potentially with write access. Remove tools the task does not need and check provider-side scopes.
- **Check actual permission behavior.** New Claude cloud sessions normally use auto mode, which reviews some actions automatically, but ask rules, repeated blocks and account settings can still pause a run. Codex schedules have their own permission settings. Test each execution environment separately.
- **Read the output and history.** A Succeeded session status does not establish that every requested file or change exists.

## Who applies the ticked triage lines

The scheduled plan step writes a proposal and a log entry. Applying a plan can move, edit or remove notes and needs a separate review.

- **Keep application interactive in this starter kit.** After reviewing and ticking entries, name the full plan path in your request. Have the agent validate each selected action, check previous apply reports, and show the intended changes before applying.
- **Keep an application record.** The report names the exact source plan and each applied, skipped or uncertain action. Skip actions already recorded as applied. If the source changed, identical capture lines are ambiguous, or a previous run stopped without a reliable report, ask before continuing.
- **Treat the reference script separately.** The reference build uses custom code to record newly created unticked plans and track application. That script is not included here, and a checkbox alone does not prove who approved it. Do not schedule note-moving or deletion with these prompts alone.

---

[Previous: Phase 3: History on GitHub (tier 2)](07-phase-3-history-on-github.md) | [Contents](../README.md#contents) | [Next: Phase 5: Phone control and an always-on machine (tier 3)](09-phase-5-always-on.md)
