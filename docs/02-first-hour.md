# Your first hour: practice before you build

Spend an hour driving an agent somewhere mistakes cost nothing: a throwaway folder. You'll learn the four moves you use every day, which are ask, approve, stop and undo.

## Terminal basics

You need a terminal for a handful of setup commands in Phase 3, and optionally to run agents. Ten minutes covers it.

- **Open one.** Windows: press Start, type Terminal, press Enter. Mac: press Cmd+Space, type Terminal, press Enter.
- **Know where you are.** The text before the cursor shows the current folder. `cd foldername` moves into a folder, `cd ..` moves up one, and `ls` lists what's here (it works on Mac and in Windows PowerShell).
- **Quote paths with spaces.** `cd "My Folder"`, not `cd My Folder`.
- **Paste and run.** Ctrl+V in Windows Terminal, Cmd+V on Mac, then Enter.
- **Stop a command.** Ctrl+C.
- **Treat errors as normal.** Copy the whole error into your agent or a chat and ask what it means and what to type next. Never paste anything containing a password or key.

## Practice session, about 45 minutes

1. **Make a sandbox.** Create a folder called `scratch` inside your AI workspace folder ([Phase 1](05-phase-1-vault-and-capture.md), step 1). Nothing important ever goes in it.
2. **Open the agent on it.** Claude: desktop app, Code tab, open `scratch`. Or in a terminal, `cd` into `scratch` and run `claude` or `codex`. Sign in when asked.
3. **Ask and approve.** Type: "Create a file called notes.md with three made-up meeting notes, each with a date and two action items." It may ask permission, depending on your mode. Review any request, then open the file to check the result.
4. **Make it show its work.** Ask: "What did you just do, step by step, and which tools did you use?" You'll see the loop drawn in [Start here](01-start-here.md).
5. **Feel the cost of vagueness.** Ask "Tidy this up." Then rewind or reset and ask "Turn each action item into a checkbox line, grouped by person. Show me the result before you save it." Compare what you got.
6. **Say no once.** If it asks permission, decline a test action and see what happens. If it does not ask, inspect the permission settings instead of assuming every write needs approval.
7. **Stop it mid-task.** Ask for something long, such as "Write 30 more fake meeting notes," then interrupt. In a terminal, press Esc. Both Claude Code and Codex show "esc to interrupt" while working. In an app, use the stop button.
8. **Undo.** In Claude Code, press Esc twice on an empty prompt, or type `/rewind`, and restore the code to before the last change. Rewind only covers edits made through its file-editing tools, not files changed by shell commands. That gap is why [Phase 3](07-phase-3-history-on-github.md) adds Git. In Codex, review the diff and ask it to reverse only this practice change. Check the restored file yourself. Neither approach recovers work that was never recorded.
9. **Write your first rule.** Create `AGENTS.md` in `scratch` with one line: "Write dates as YYYY-MM-DD and end every reply with one suggested next step." For Claude, also create `CLAUDE.md` containing `@AGENTS.md`. Start a new session and give it any task. Check whether the response follows the rule and which instruction file loaded. A rule guides behavior, so verify its effect rather than assuming it took effect.
10. **Check a claim.** Ask "How many meeting notes are in notes.md now?" Then open the file and count. Note whether its answer matched.

When these moves feel routine, start [Phase 1](05-phase-1-vault-and-capture.md).

---

[Previous: Start here: how the pieces think](01-start-here.md) | [Contents](../README.md#contents) | [Next: Architecture](03-architecture.md)
