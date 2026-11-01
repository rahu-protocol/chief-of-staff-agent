# Starter kit

Everything in [`ai-workspace/`](ai-workspace/) is meant to be copied into your own AI workspace folder, such as `C:\ai\` or `~/ai/`. Copy it, then open `vault` in Obsidian with Open folder as vault. Don't work inside the downloaded repo, or your notes end up mixed with the playbook's files.

These are the reference build's working files, generalized. Edit the folder names and data rules to fit you.

| File | What it does | Edit it? |
| --- | --- | --- |
| [`AGENTS.md`](ai-workspace/AGENTS.md) | Shared rules for every agent: folders, where agents may write, background job rules, data rules, external actions | Yes: the data rules line in brackets is yours to fill |
| [`CLAUDE.md`](ai-workspace/CLAUDE.md) | One line, `@AGENTS.md`, so Claude Code reads the same rules as Codex | No |
| `scratch/` | Throwaway workspace for tests and drafts | No |
| [`vault/AGENTS.md`](ai-workspace/vault/AGENTS.md) | Note rules: properties, folders, inbox triage plan format, lessons | Only if you change the schema |
| [`vault/CLAUDE.md`](ai-workspace/vault/CLAUDE.md) | Same one-line pointer for the vault | No |
| [`vault/.obsidian/app.json`](ai-workspace/vault/.obsidian/app.json) | Obsidian settings: new notes to `Inbox`, attachments to `Attachments`, links updated on rename, deletes to `.trash` | Check them once in Settings, Files and links |
| [`vault/.gitignore`](ai-workspace/vault/.gitignore) | Keeps window layouts and the trash out of Git | No |
| [`vault/Inbox/Capture.md`](ai-workspace/vault/Inbox/Capture.md) | The capture log your phone appends to | No |
| [`vault/Inbox.base`](ai-workspace/vault/Inbox.base) | Inbox backlog, oldest first | No |
| [`vault/Projects.base`](ai-workspace/vault/Projects.base) | Active projects, plus a view of those untouched for 14 days | No |
| [`vault/Tasks.base`](ai-workspace/vault/Tasks.base) | Open tasks by due date | No |
| [`vault/Context/`](ai-workspace/vault/Context/) | `Me`, `Priorities`, `Working with me` and `Decisions` starters | Yes, or let the onboarding interview draft them |
| `vault/People/` | One note per person you work with | The agent proposes these |
| [`vault/agents/prompts/`](ai-workspace/vault/agents/prompts/) | The nine prompts from the [prompt library](../docs/11-prompt-library.md) | Improve them over time |
| [`vault/agents/log.md`](ai-workspace/vault/agents/log.md) | One line per agent job | Agents append |
| `vault/agents/outputs/` | Plans, briefs and reviews, one dated file per run | Agents write here |
| Empty folders | `Projects`, `Areas`, `Tasks`, `Notes`, `Archive`, `Attachments`. Each holds a hidden `.gitkeep` file so Git keeps the folder | No |

The `.base` files and `app.json` were written from Obsidian's documented syntax and settings. If a view's sort or filter misbehaves, set it once from the view's menu in Obsidian and it rewrites the file.
