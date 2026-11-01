# Phase 2: Rules and the chief of staff (tier 1)

This phase turns a generic agent into yours. The rules file says how the system works. A small set of context notes says who you are and what matters now. About an hour, half of it an interview.

1. **Install the agent and point it at the vault.**
   - Claude: in the desktop app's Code tab, open the `vault` folder. From a terminal, `cd` into the vault and run `claude`.
   - Codex: in the Codex app, add the `vault` folder as a project. From a terminal, `cd` into the vault and run `codex`.
   - Use restricted permissions and review their scope. A default mode may allow workspace reads and writes without asking. Test an allowed practice edit and a blocked action before using personal notes.
2. **Install the Obsidian skills.** These teach the agent wikilinks, properties, Bases and Canvas, so its notes look like yours.
   - Claude Code: `/plugin marketplace add kepano/obsidian-skills`, then `/plugin install obsidian@obsidian-skills`.
   - Codex and other agents: `npx skills add https://github.com/kepano/obsidian-skills` (needs Node.js).
   - Two of the skills reach outside the vault: `defuddle` fetches web pages and `obsidian-cli` drives the Obsidian app. Their tools inherit the access you grant, so review their capabilities separately.
3. **Write the rules.** The starter kit has both rules files: [`AGENTS.md`](../starter-kit/ai-workspace/AGENTS.md) for the workspace and [`vault/AGENTS.md`](../starter-kit/ai-workspace/vault/AGENTS.md) for the vault. Edit the folder list and data rules to fit you. Next to each sits a `CLAUDE.md` containing one line, `@AGENTS.md`, so Claude Code reads the same rules. Building by hand? Copy those four files. Start a fresh session and check that it reads both the vault rules and the parent workspace rules, including after the vault becomes a Git repo. Instruction files guide behavior, while tool settings enforce access.
4. **Create the context layer.** Add a `Context` folder and a `People` folder. These are the chief of staff's working memory about you. The starter kit includes both, with [starter notes](../starter-kit/ai-workspace/vault/Context/) to fill in.

| Note | Holds | Who edits |
| --- | --- | --- |
| `Context/Me.md` | Role, responsibilities, working hours, goals for the year | You; agent proposes changes |
| `Context/Priorities.md` | The 3 to 5 things that matter most right now, each linked to a project or area | You, at the weekly review |
| `Context/Working with me.md` | How the agent should write, what to escalate, what never to do, corrections you've given | Agent appends approved lessons |
| `Context/Decisions.md` | One dated line per decision: what, why, when to revisit | Agent drafts, you approve |
| `People/<Name>.md` | Who they are, how you work together, open items with them | Agent proposes, you approve |

Keep each context note under a page. Agents read them at the start of most jobs, so length costs time and usage on every run.

5. **Run the onboarding interview.** Start a session in the vault and type `Follow agents/prompts/onboarding-interview.md`, or paste the [onboarding prompt](../starter-kit/ai-workspace/vault/agents/prompts/onboarding-interview.md). The agent asks questions, then writes a uniquely named plan containing proposed context and project notes. Tick the entries you approve and ask an interactive session to apply that exact plan path. Review the changed files and its apply report.
6. **Use it the same day.** Ask it what to work on today, to draft a reply using what it knows about the person, or to turn a messy meeting note into tasks. Each correction you make is raw material for Phase 6.

The reference build covers steps 1 to 3. The context layer and interview are additions for the chief-of-staff role, built on the same rules: the agent proposes, you approve.

---

[Previous: Phase 1: Vault and capture (tier 1)](05-phase-1-vault-and-capture.md) | [Contents](../README.md#contents) | [Next: Phase 3: History on GitHub (tier 2)](07-phase-3-history-on-github.md)
