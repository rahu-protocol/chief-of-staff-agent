# Verification status and sources

Product sources reviewed November 1, 2026. Separate reported reference-build experience, checks against documentation, and live tests. A documentation correction does not certify runtime behavior.

| Part | Status |
| --- | --- |
| Vault layout, capture log, log format and Inbox.base | Reported running in the reference build. This cleanup reviewed the public templates and changed naming and approval instructions. |
| Sync to phone and tablet, and first private-vault GitHub push | Reported tested in the reference build. Not repeated during this documentation cleanup. |
| Automatic desktop Git commits | Configured in the reference build, but no automatic commit had landed at the original review. Confirm a second automatic push and a sample restore yourself. |
| Scheduled triage and digest jobs | Reported runs used a custom local harness and OS scheduler. The reported triage run had an empty inbox. This does not validate the public prompts on populated input. |
| Claude scheduling, Remote Control, memory and instruction loading | Checked against official documentation November 1, 2026. Not run end to end against this starter vault. Cloud tasks can still pause for approval. |
| Codex schedules, mobile access, instruction loading and permissions | Checked against official OpenAI documentation November 1, 2026. Availability and execution location depend on account, workspace and selected environment. No live scheduler or mobile test here. |
| Context notes, People notes, interview, brief and review prompts | Designed for this playbook. Not yet run end to end. Approved-plan and repeat-run instructions were clarified, not implemented as a separate application engine. |
| Projects.base, Tasks.base and starter app settings | Written from documented formats. No new live Obsidian validation in this cleanup. |
| Recovery and conflict handling | Git records committed snapshots, and GitHub holds pushed commits. Unique filenames and one writer reduce conflicts. This kit provides no automatic locking or authenticated approval service. |
| AI and Sync price examples | Checked against vendor pricing and plan pages November 1, 2026. US examples exclude tax and may change. Confirm local checkout and access before buying. |
| Local-model performance numbers | Reported observations from the reference build. Its benchmark logs are not distributed here and the numbers were not independently reproduced. |

## Before publishing an installment

Recheck its prices, menu labels, scheduling rules and mobile access against the vendor pages. Record the review date, product version where known, execution location and account limitations. Keep untested steps labeled until a watched run and file readback establish the result.

For recovery claims, demonstrate restoring a disposable committed note. For repeat-run claims, use populated captures, run twice on the same day, approve only selected items and verify that a second apply does not duplicate them. These remain reader or release checks until recorded as completed.

## Privacy before a public release

Review the exact files being published, document metadata and embedded examples, screenshots, and reachable Git history. Check commit author identity separately from document contents. A prior review describes the version it examined and does not automatically cover later edits. Keep private vault data out of this public starter-kit repository.

## Primary sources

- [Claude Code memory, AGENTS.md and imports](https://code.claude.com/docs/en/memory)
- [Claude Code permissions](https://code.claude.com/docs/en/permissions)
- [Claude Code desktop scheduled tasks](https://code.claude.com/docs/en/desktop-scheduled-tasks)
- [Claude Code cloud scheduled tasks and approval behavior](https://code.claude.com/docs/en/web-scheduled-tasks)
- [Claude Code Remote Control](https://code.claude.com/docs/en/remote-control)
- [Claude Code checkpoints and recovery limits](https://code.claude.com/docs/en/checkpointing)
- [Claude plan pricing](https://claude.com/pricing)
- [Codex instruction discovery](https://learn.chatgpt.com/docs/agent-configuration/agents-md)
- [Codex approvals and access controls](https://learn.chatgpt.com/docs/agent-approvals-security)
- [OpenAI scheduled tasks](https://learn.chatgpt.com/docs/automations)
- [OpenAI plan pricing](https://learn.chatgpt.com/docs/pricing)
- [OpenAI remote connections and mobile access](https://learn.chatgpt.com/docs/remote-connections)
- [Obsidian Sync pricing](https://obsidian.md/sync)
- [Obsidian Sync plans and storage limits](https://obsidian.md/help/sync/plans)
- [Obsidian mobile Quick Capture release](https://obsidian.md/changelog/2026-10-05-mobile-v1.14.4/)
- [Obsidian iOS capture options](https://obsidian.md/help/ios)
- [Obsidian Bases syntax](https://obsidian.md/help/bases/syntax)
- [Obsidian Git maintainer documentation](https://github.com/Vinzent03/obsidian-git)
- [Obsidian skills maintainer documentation](https://github.com/kepano/obsidian-skills)
- [Git snapshots and recording changes](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)
- [GitHub plans and private repositories](https://docs.github.com/en/get-started/learning-about-github/githubs-plans)
- [Ollama context length and current defaults](https://docs.ollama.com/context-length)
- [Microsoft Remote Desktop setup](https://support.microsoft.com/en-us/windows/how-to-use-remote-desktop-5fe128d5-8fb1-7a23-3b8a-41e636865e8c)
- [Tailscale key expiry](https://tailscale.com/kb/1028/key-expiry)
- [Tailscale access grants](https://tailscale.com/kb/1324/grants)

---

[Previous: Glossary](15-glossary.md) | [Contents](../README.md#contents)
