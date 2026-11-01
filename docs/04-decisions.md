# Decisions before you start

Make four decisions first. Each one is cheap now and annoying to reverse later.

**1. Which agent.** Use whichever AI subscription you already pay for. Both work with this design because both read `AGENTS.md`.

| Option | Agent | Entry price (third-party reports, check vendor) | Scheduling | Phone access to a desktop session |
| --- | --- | --- | --- | --- |
| Claude Pro or Max | Claude Code (desktop app Code tab, or terminal) | Pro $20/month, $17/month billed annually; Max from $100 | Local tasks on your computer, or cloud tasks that run with it off | Remote Control from the Claude app |
| ChatGPT Plus or Pro | Codex (desktop app, or terminal) | Plus $20/month; Pro from $100 | Automations in the Codex app, local runs need the app open | Check current Codex docs |
| Both | Both on the same vault | Sum of the two | Pick one scheduler so jobs don't double up | Either |

**2. Which machine.** Tiers 1 and 2 run fine on a laptop you use daily. Tier 3 wants a computer that stays on, because local scheduled tasks only fire while the app is open and the computer is awake. On Windows, keep the vault out of folders synced by OneDrive (Documents is often redirected there). File-sync clients and agents editing the same files make a poor combination.

**3. What stays out of the vault.** Anything in the vault reaches your phone, Obsidian's sync servers (encrypted), your GitHub repo, and the AI vendor whenever an agent reads it. Decide now what never goes in: passwords and keys, other people's sensitive data, and anything your employer's AI or data policy forbids on personal accounts. Write that decision into the rules file so agents enforce it too.

**4. Budget.** Obsidian itself is free.

| Item | Cost | Limits that matter |
| --- | --- | --- |
| Obsidian Sync Standard | $4/month billed annually, $5 monthly | 1 synced vault, 1 GB, 5 MB per file, 1 month of version history |
| Obsidian Sync Plus | $8/month billed annually | 10 vaults, 10 GB, 200 MB per file |
| GitHub private repo | Free | GitHub keeps every commit, which covers Sync's short history |
| AI subscription | See table above | Agent sessions and scheduled runs draw from the same usage allowance |

Standard is enough for a notes vault. Upgrade only if you hit the 5 MB file limit with PDFs or images, or want a separate work vault.

---

[Previous: Architecture](03-architecture.md) | [Contents](../README.md#contents) | [Next: Phase 1: Vault and capture (tier 1)](05-phase-1-vault-and-capture.md)
