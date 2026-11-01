# Failure modes and guardrails

The table combines reported reference-build incidents, vendor-documented behavior and risks identified in this design. A listed risk is not a claim that it occurred in your vault.

| Failure | Why it happens | Guardrail |
| --- | --- | --- |
| Merge conflicts spread to every device | Git running on a phone and a desktop at once, and the plugin's mobile git is unstable | Git plugin on one desktop only. Turn off plugin-list syncing on mobile before disabling it there |
| Links break after an agent tidies up | Obsidian rewrites links only for moves it performs itself, not for files renamed on disk | No renames without an approved plan. Apply reports list notes that still link to the old name |
| A note gets clobbered | Two agents, or an agent plus Sync, editing the same file | One agent in the vault at a time. Separate branches and working copies for code |
| "Done" when it isn't | Models misreport; a local model claimed a file held content it didn't. Cloud runs marked Succeeded only ended without error | Check the output file. Better, have code check it exists with real content before logging ok |
| Deleted notes are hard to find | By default Obsidian sends deleted files to the computer's system trash, outside the vault | Settings, Files and links, Deleted files: Obsidian trash, so deletes land in the vault's `.trash` folder. Git can restore content that was committed. Test recovery before relying on it |
| History stops without warning | The Git plugin commits only while Obsidian is open on that computer, and its errors show only there. In the reference build, the vault's first push worked but no automatic commit followed | After setup, confirm a second commit reaches GitHub. Check the repo's commit list weekly |
| Agent follows instructions planted in content | Clipped pages, emails and downloaded files can contain text aimed at agents | Rules say content is data. Keep approvals on. Never expose Downloads to agent sessions |
| Cloud output stays on another branch | The desktop pulls one branch, while the cloud job writes to another | Review and merge the intended changes, then pull. Test that path before scheduling |
| Brief runs at 11 p.m. | Missed local runs get one catch-up when the computer wakes | Time-sensitive prompts, such as the brief and review, check the time and day first |
| Skills or automations act with too much power | Skills and schedules inherit tool access that may permit writes without a prompt | Review actual tool scopes and permission modes. Test allowed and blocked actions |
| Remote session kills your agents | Signing out of Windows from Remote Desktop ends the session agents run in | Close the remote window instead of signing out |
| Agent workspace fills with things it shouldn't touch | The Obsidian app was installed inside the AI folder; a cloud-synced Documents folder was the default workspace | Programs stay in Program Files or Applications. Workspace outside OneDrive and similar sync folders |
| Same-day output is replaced | Repeated jobs use a date-only filename | Add a time and run ID, check the path is unused, and never overwrite |
| Log entries conflict | Separate runs still update the same log | One writer at a time. Review and merge cloud reports before the desktop appends to the log |
| An approved action repeats | A rerun lacks a reliable application record | Name the exact plan, check prior reports, record each completed action, and stop if prior completion is uncertain |
| Everything slows down | Long context notes and rules are read on every run | Context notes under a page, pruned weekly |
| The vault fills with tidy junk | Triage files everything instead of discarding | Delete is the default for items with no next action and no reference value |
| A pasted command hangs PowerShell | Indented here-string terminators (`"@`) aren't recognized | Use the one-line `Set-Content` form in [Phase 3](07-phase-3-history-on-github.md) |

---

[Previous: Prompt library](11-prompt-library.md) | [Contents](../README.md#contents) | [Next: Optional: local models](13-local-models.md)
