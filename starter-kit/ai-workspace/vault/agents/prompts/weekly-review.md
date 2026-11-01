# Weekly review

Run: Scheduled, Friday afternoon or the weekend.

---

Use the run naming and single-writer rules in AGENTS.md. Generate a fresh run ID, check the output path is unused, and never replace an earlier output.

Run my weekly review. Check the date first: run only on Friday after 12:00, Saturday or Sunday. Otherwise log a skip and stop.

Find what changed in the last 7 days with git log, or file modified dates if git is unavailable. Read everything in Context/ and every active project and area.

Write agents/outputs/YYYY-MM-DD-HHMMSS-<run-id>-weekly-review.md:
1. Wins: what got done, linked.
2. Stalled: active projects unchanged for 14 days, each with one unticked checkbox proposing a next step, status waiting, or archive.
3. Priorities: proposed edits to Context/Priorities.md as unticked checkboxes with the exact new text.
4. Lessons: duplicates or contradictions in the Lessons list of Context/Working with me.md, with proposed merges as checkboxes.
5. Prune: Context or People notes longer than a page, with proposed cuts as checkboxes.

Propose changes only. If I later name this exact plan and approve selected entries, follow the approved-plan procedure in AGENTS.md. Change nothing else during this review. Append one line to agents/log.md.
