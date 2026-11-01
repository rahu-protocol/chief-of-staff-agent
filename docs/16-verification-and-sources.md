# Verification status and sources

Agent products change monthly. This table says how much weight each part of the playbook can bear.

| Part | Status |
| --- | --- |
| Vault layout, rules files, triage plan format, capture log, log format, `Inbox.base` | Running in the reference build; copied from its files |
| Sync to phone and tablet; a session started from a tablet creating a note that synced back | Tested end to end in the reference build |
| First push of the vault to a private GitHub repo | Tested in the reference build |
| Automatic commits from the Git plugin | Configured in the reference build, but no automatic commit had landed at the time of writing |
| Scheduled triage and digest jobs | Ran in the reference build on its local harness and the OS task scheduler, not the agent apps' schedulers. The triage run so far found an empty inbox |
| Claude local and cloud scheduled tasks, Remote Control from a phone | From vendor docs; cloud scheduled tasks are a research preview. Not yet run against this vault layout |
| Codex automations and mobile access | From vendor overview pages; click paths not verified here |
| Context folder, People notes, onboarding interview, brief and review prompts | Designed for this playbook; not yet run end to end |
| `Projects.base`, `Tasks.base`, the starter `.obsidian/app.json` | Written from Obsidian's documented syntax and settings; untested |
| AI plan prices | Third-party reports; check vendor pricing pages |

Sources:

- [Claude Code: cloud scheduled tasks](https://code.claude.com/docs/en/web-scheduled-tasks.md)
- [Claude Code: Desktop scheduled tasks](https://code.claude.com/docs/en/desktop-scheduled-tasks.md)
- [Claude Code: Remote Control](https://code.claude.com/docs/en/remote-control)
- [Claude Code reads AGENTS.md (v2.1.277+)](https://www.developersdigest.tech/blog/claude-code-agents-md-support)
- [OpenAI Academy: Codex automations](https://openai.com/academy/codex-automations)
- [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills/wiki)
- [Obsidian Sync Standard plan](https://obsidian.md/blog/standard-plan/)
- [Obsidian help: iOS widgets, Shortcuts, Siri](https://obsidian.md/help/ios)
- [Obsidian mobile 1.14.4 changelog: Quick Capture](https://obsidian.md/changelog/2026-10-05-mobile-v1.14.4/)
- [Obsidian help: Bases syntax](https://obsidian.md/help/bases/syntax)
- [Obsidian Git plugin](https://github.com/Vinzent03/obsidian-git)
- [Claude Code pricing (third-party)](https://www.softr.io/blog/claude-code-pricing)
- [Codex pricing (third-party)](https://www.nocode.mba/articles/codex-pricing)
- [Codex issue: synced folders as workspaces](https://github.com/openai/codex/issues/22532)
- [Agent framework system prompt overwhelming small models](https://github.com/NousResearch/hermes-agent/issues/25041)
- [Ollama default context length](https://github.com/NousResearch/hermes-agent/issues/43900)

---

[Previous: Glossary](15-glossary.md) | [Contents](../README.md#contents)
