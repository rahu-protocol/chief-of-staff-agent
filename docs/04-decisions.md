# Decisions before you start

Make four decisions first. Each one is cheap now and annoying to reverse later.

**1. Which agent.** Use an agent you already have access to. Verify that your plan includes the local tools you need before buying another subscription. Prices below are US list-price examples checked November 1, 2026, before tax. Check the linked vendor pages for current regional pricing and feature access.

| Option | Agent | Price example and primary source | Scheduling | Phone access to a desktop session |
| --- | --- | --- | --- | --- |
| Claude paid plan | Claude Code on desktop or in a terminal | Pro $20 monthly or $200 annually; Max $100 monthly. See [Claude pricing](https://claude.com/pricing) for other plans | Desktop local tasks and cloud scheduled tasks have different access and permissions | [Remote Control](https://code.claude.com/docs/en/remote-control) on supported plans |
| ChatGPT plan with Codex | Codex on desktop or in a terminal | Plus $20 monthly; Pro from $100 monthly. See [OpenAI pricing](https://learn.chatgpt.com/docs/pricing) for all plans | Local project schedules need the computer and app running. Cloud tasks have different file access | [Mobile remote connections](https://learn.chatgpt.com/docs/remote-connections), subject to rollout and workspace settings |
| Both | Both using the same approved context | Pay only for plans you need | Choose one scheduler and run one vault writer at a time | Check the relevant host and mobile requirements |

**2. Which machine.** Tiers 1 and 2 can run on your daily laptop. Jobs that need local files require that computer to be awake and the app running. On Windows, keep the vault outside OneDrive and other overlapping sync folders. Tier 3 adds an always-on machine only if your work needs one.

**3. What stays out of the vault.** Selected vault content can reach your synced devices, GitHub after a push, and an AI service when an agent reads it. Decide what stays out: passwords, keys, other people's sensitive data, and material your employer forbids on personal accounts. Write the boundary into the rules and enforce access limits in tool settings too.

**4. Budget.** Obsidian itself is free. Sync examples below come from [Obsidian pricing](https://obsidian.md/sync) and [plan limits](https://obsidian.md/help/sync/plans), checked November 1, 2026.

| Item | Cost example | Limits that matter |
| --- | --- | --- |
| Obsidian Sync Standard | $4 per month billed annually, $5 billed monthly | 1 vault, 1 GB, 5 MB per file, 1 month of version history |
| Obsidian Sync Plus | $8 per month billed annually, $10 billed monthly | 10 vaults, 10 GB base storage, 200 MB per file, 12 months of version history |
| Private GitHub repository | Available on [GitHub Free](https://docs.github.com/en/get-started/learning-about-github/githubs-plans) | Stores commits you push. It does not capture edits between commits |
| AI subscription | See the vendor pages above | Agent and scheduled usage depends on plan, model and execution environment. API billing may be separate |

Start with Standard if its file and storage limits fit your notes. Before publishing an installment, recheck its prices, menu labels, scheduling rules and mobile availability against current vendor documentation and record the review date.

---

[Previous: Architecture](03-architecture.md) | [Contents](../README.md#contents) | [Next: Phase 1: Vault and capture (tier 1)](05-phase-1-vault-and-capture.md)
