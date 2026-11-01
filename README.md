# Chief of Staff Agent

A playbook and starter kit for building a personal chief of staff agent with Obsidian, GitHub and a frontier agent such as Claude Code or Codex. The core setup needs no coding.

Product sources reviewed November 1, 2026. Agent products change monthly, so [Verification status and sources](docs/16-verification-and-sources.md) marks what was tested and what comes from vendor docs.

You build a chief of staff agent around a shared folder of Markdown notes. Your phone captures new work, an agent such as Claude Code or Codex reads the relevant notes, and rules describe what it may change. Approved priorities, decisions and corrections go into the vault so you can inspect them and use them with another agent.

The working rule is **propose, approve, apply**. Changes to existing notes start as a plan you review. Approved deletes go to the vault trash. Git can restore committed snapshots once history is configured and checked. Written rules guide the agent, while tool permissions control what it can actually do.

This playbook comes from a working reference build: an Obsidian vault synced to phone and tablet, backed up to a private GitHub repo, worked on by Claude Code and Codex under a shared rules file, with scheduled triage and digest jobs. That build also runs local models. Most people should skip that part, so it sits in an optional section at the end.

| Tier | What you get | Setup time (estimate) | Skill needed |
| --- | --- | --- | --- |
| 1. Core | Vault on every device, one-tap capture from your phone, an agent that reads and writes the vault under your rules | 2 hours | None |
| 2. Loops | Committed history on GitHub, scheduled inbox triage, a morning brief and a weekly review you approve by ticking boxes | 2 to 3 more hours | Pasting terminal commands |
| 3. Always-on | A dedicated machine, agent sessions started from your phone, agents in separate working copies, email and calendar connected | A weekend | Comfortable in a terminal |

Stop at whichever tier covers what you need. Tier 1 gives you a shared, editable record of context that works alongside an agent's built-in memory.

## Quick start

1. **New to AI agents?** Read [Start here](docs/01-start-here.md), then do [Your first hour](docs/02-first-hour.md) in a throwaway folder. The [Glossary](docs/15-glossary.md) defines every term.
2. **Get the files.** On this repo's page, click Code, then Download ZIP, and unzip it. Or clone it with Git.
3. **Copy the starter kit.** Copy everything inside [`starter-kit/ai-workspace/`](starter-kit/ai-workspace/) into a new folder for your AI work, such as `C:\ai\` or `~/ai/`. Work in the copy, not in the downloaded repo.
4. **Follow the phases in order.** [Phase 1](docs/05-phase-1-vault-and-capture.md) and [Phase 2](docs/06-phase-2-rules-and-context.md) give you a working tier 1 system. Add later phases when you want them.

## Contents

| # | Chapter | What's in it |
| --- | --- | --- |
| 1 | [Start here: how the pieces think](docs/01-start-here.md) | Plain-language concepts: model, agent, context, and why the design looks the way it does |
| 2 | [Your first hour: practice before you build](docs/02-first-hour.md) | Terminal basics and a safe practice session: ask, approve, stop, undo |
| 3 | [Architecture](docs/03-architecture.md) | The five parts, how they connect, and seven design principles |
| 4 | [Decisions before you start](docs/04-decisions.md) | Which agent, which machine, what stays out, and the budget |
| 5 | [Phase 1: Vault and capture (tier 1)](docs/05-phase-1-vault-and-capture.md) | Vault, folders and one-tap capture from your phone |
| 6 | [Phase 2: Rules and the chief of staff (tier 1)](docs/06-phase-2-rules-and-context.md) | Rules files, context notes and the onboarding interview |
| 7 | [Phase 3: History on GitHub (tier 2)](docs/07-phase-3-history-on-github.md) | Version history and undo with Git and a private GitHub repo |
| 8 | [Phase 4: Daily and weekly loops (tier 2)](docs/08-phase-4-daily-and-weekly-loops.md) | Scheduled triage, morning brief and weekly review |
| 9 | [Phase 5: Phone control and an always-on machine (tier 3)](docs/09-phase-5-always-on.md) | An always-on machine, phone control and safe multi-agent work |
| 10 | [Phase 6: Connectors, and how it compounds](docs/10-phase-6-connectors.md) | Email and calendar connectors, and how the agent improves over time |
| 11 | [Prompt library](docs/11-prompt-library.md) | The nine prompts and when to run each |
| 12 | [Failure modes and guardrails](docs/12-failure-modes.md) | What goes wrong and the guardrail for each |
| 13 | [Optional: local models](docs/13-local-models.md) | Lessons from running a local model as a background agent |
| 14 | [Learning path](docs/14-learning-path.md) | The skill each stage builds and where it transfers |
| 15 | [Glossary](docs/15-glossary.md) | Every term in one line |
| 16 | [Verification status and sources](docs/16-verification-and-sources.md) | What was tested, what comes from vendor docs, and sources |

## Repo layout

```
docs/                    the playbook, one chapter per file
starter-kit/
  ai-workspace/          copy this folder's contents to start
    AGENTS.md            shared rules for every agent
    CLAUDE.md            one line that points Claude Code at AGENTS.md
    scratch/             throwaway workspace
    vault/               a ready-to-open Obsidian vault
      AGENTS.md          note schema, folders and inbox triage rules
      Context/           who you are and what matters now
      agents/prompts/    the nine prompts
      agents/log.md      one line per agent job
      Inbox.base, Projects.base, Tasks.base   table views
```

The [starter kit guide](starter-kit/README.md) explains every file.

## License

MIT. See [LICENSE](LICENSE). Obsidian, GitHub, Claude Code, Codex and the other products named here belong to their makers. This project is independent and not affiliated with any of them.
