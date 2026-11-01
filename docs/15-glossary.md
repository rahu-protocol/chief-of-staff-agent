# Glossary

| Term | Meaning |
| --- | --- |
| Agent | An AI model running in a loop with tools, able to read and write files, run commands and check results until a task is done |
| `AGENTS.md` | A plain-text rules file that agents read before acting. Codex reads it natively; Claude Code reads it directly or through `CLAUDE.md` |
| Approval, permission prompt | The agent pausing to ask before it runs a command or changes a file |
| Area | An ongoing responsibility with no end date, such as health or finances |
| Base (`.base`) | An Obsidian file that defines table or board views over notes and their properties |
| Branch | A parallel line of changes in a Git repo, kept apart until merged |
| Catch-up run | A single run a local scheduled task makes on wake after a time it missed while the computer slept |
| Checkpoint, rewind | Claude Code's automatic snapshots of its own file edits, which you can restore with `/rewind` |
| `CLAUDE.md` | Claude Code's own rules file. A one-line `@AGENTS.md` inside it imports the shared rules |
| Clone | A full copy of a Git repo, history included |
| Cloud task, local task | A scheduled task running on the vendor's servers (computer can be off, sees only GitHub) or on your machine (sees your files, needs the computer awake) |
| Commit | One saved snapshot in Git, with a message saying what changed |
| Connector, MCP | A plug-in that links an agent to an outside service. MCP, the Model Context Protocol, is the open standard most connectors use |
| Context notes | The notes in `Context/` that tell the agent who you are, what matters now and how to work with you |
| Context window | The text a model can see at once in a session. It is cleared when the session ends |
| Frontmatter, properties | The labeled values at the top of a note, between two `---` lines |
| Git | Software that records every version of every file in a folder |
| GitHub | A website that hosts Git repos, private or public |
| `.gitignore` | A list of files Git should not track |
| Inbox triage | Sorting new captures into tasks, notes, projects or deletions through a plan you approve |
| Markdown | Plain text with light formatting symbols, saved as `.md` files |
| Model | The AI itself, such as Claude or GPT: text in, text out |
| Obsidian | A free app for reading, writing and linking a folder of Markdown notes |
| Obsidian Sync | Obsidian's paid, end-to-end encrypted service that keeps a vault the same across devices |
| Plan | A file of unticked checkbox lines describing changes an agent proposes. Only ticked lines get applied |
| Project | Work with an outcome and an end date |
| Prompt | The instructions you give a model or agent |
| Prompt injection | Text hidden in an email, web page or file that tries to steer an agent into doing something you didn't ask |
| Pull, push | Downloading changes from GitHub, and uploading your commits to it |
| Remote Control | A Claude Code feature that lets the Claude mobile app steer a session running on your computer |
| Repository, repo | A folder tracked by Git, along with its full history |
| Scheduled task | A saved prompt that runs automatically on a timer |
| Skill | A packaged set of instructions, and sometimes scripts, that teaches an agent a specific job |
| Tailscale | A service that puts your devices on a private network so they can reach each other from anywhere |
| Terminal, CLI | A text window for typing commands; a CLI is a program you run from it |
| Token | The unit models count text in, roughly three quarters of an English word |
| Usage allowance | The amount of model use your subscription includes per period, shared by chat, agent sessions and scheduled jobs |
| Vault | An Obsidian notebook: a normal folder of Markdown files plus Obsidian's settings |
| Wikilink | A link between notes written as `[[Note name]]` |
| Worktree | A second working copy of a Git repo on its own branch, so two agents can work without colliding |

---

[Previous: Learning path](14-learning-path.md) | [Contents](../README.md#contents) | [Next: Verification status and sources](16-verification-and-sources.md)
