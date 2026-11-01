# Phase 1: Vault and capture (tier 1)

The goal of this phase is one inbox you can reach from your phone in two seconds, and a vault that routes everything new into it. About an hour.

1. **Make an AI workspace folder.** Create one parent folder for all AI work, such as `C:\ai\` on Windows or `~/ai/` on a Mac. The vault goes inside it, and future projects sit beside it. Agents then have one place to work and one place to be told the rules.
2. **Create the vault.** Install Obsidian on your computer. Fastest route: copy everything inside [`starter-kit/ai-workspace/`](../starter-kit/ai-workspace/) into your workspace folder, then in Obsidian choose Open folder as vault and pick the `vault` folder. The starter vault already has the folders, settings, rules, views and prompts, so check the settings in step 4 and go on to step 6. To build it by hand instead, choose Create new vault, name it `vault`, set the location to the workspace folder, and click Create.
3. **Add the folders.** Create `Inbox`, `Projects`, `Areas`, `Tasks`, `Notes`, `Archive`, `Attachments` and `agents/outputs`. Keep it flat. Properties and links do the sorting, not nested folders.
4. **Route new material.** In Settings, Files and links:
   - Default location for new notes: In the folder specified below, then `Inbox`.
   - Default location for new attachments: `Attachments`, so phone photos and PDFs don't swell the inbox.
   - Automatically update internal links: on.
   - Deleted files: Obsidian trash, so deletes land in the vault's `.trash` folder instead of your computer's trash.
5. **Add the capture log and backlog view.** Copy [`Inbox/Capture.md`](../starter-kit/ai-workspace/vault/Inbox/Capture.md) and [`Inbox.base`](../starter-kit/ai-workspace/vault/Inbox.base) from the starter kit. The base lists everything in the inbox, oldest first. Keep it open as a tab.
6. **Turn on Obsidian Sync.** On the computer, Settings, Core plugins, Sync, then create a remote vault and connect. Install Obsidian on phone and tablet, sign in, and connect each to the same remote vault.
7. **Set up one-tap capture.**
   - iPhone or iPad on iOS 26: use Obsidian's Quick Capture. Create a Location that appends to `Inbox/Capture.md`, then put it on the Lock Screen, in Control Center, or on the Action button.
   - Older iOS: in the Shortcuts app, use Obsidian's Capture action to append to `Inbox/Capture.md`. If the action only offers bookmarked notes, bookmark `Inbox/Capture.md` in Obsidian first. Siri also responds to "Capture to Obsidian."
   - Android: add Obsidian's New Note widget. New notes land in `Inbox` because of step 4.
8. **Adopt one habit.** Start every capture with what it is: `task`, `idea`, `ref`, or a project name. It costs one word and makes triage far more accurate. Long dictation gets its own note, and one-liners go to the capture log.
9. **Test it.** Capture a line from your phone. It should appear in `Inbox/Capture.md` on the computer within about a minute.

Mobile menu labels change between releases. If a label above doesn't match, search the app's settings for the nearest equivalent.

---

[Previous: Decisions before you start](04-decisions.md) | [Contents](../README.md#contents) | [Next: Phase 2: Rules and the chief of staff (tier 1)](06-phase-2-rules-and-context.md)
