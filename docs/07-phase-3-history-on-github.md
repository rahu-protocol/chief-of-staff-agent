# Phase 3: History on GitHub (tier 2)

Git gives you undo for anything an agent does, and GitHub gives cloud agents a copy of the vault to work from. Do this before you let any job run unattended. About 30 minutes.

1. **Install Git and the GitHub CLI.** Windows: `winget install --id Git.Git` and `winget install --id GitHub.cli`. Mac: install Git from git-scm.com and the CLI from cli.github.com. Close and reopen the terminal afterwards so it finds the new commands.
2. **Sign in once.**

```
gh auth login
git config --global user.name "Your Name"
git config --global user.email "your-id@users.noreply.github.com"
```

In `gh auth login`, choose GitHub.com, HTTPS and browser login. That also sets up Git's credentials. Your noreply address is under GitHub Settings, Emails. Using it keeps your real email out of commit history.

3. **Put the vault in a private repo.** From inside the vault folder:

```
git init -b main
```

Then create the `.gitignore`, unless you used the starter vault, which already has one. PowerShell:

```
Set-Content .gitignore -Value ".obsidian/workspace.json", ".obsidian/workspace-mobile.json", ".trash/"
```

Mac or Linux:

```
printf '%s\n' .obsidian/workspace.json .obsidian/workspace-mobile.json .trash/ > .gitignore
```

Then commit and push:

```
git add -A
git commit -m "Initial vault"
gh repo create my-vault --private --source . --remote origin --push
```

The last command prints the new repo's URL. The ignored files are window layouts that change constantly, and the trash.

4. **Auto-commit from the desktop.** In Obsidian on the computer: Settings, Community plugins, turn them on, Browse, install and enable **Git** by Vinzent03. Set the automatic commit-and-sync interval to 10 minutes and turn on pull on startup. If you enabled the plugin before the folder was a repo, restart Obsidian.
5. **Keep Git off your phone and tablet.** The plugin's author calls its mobile version very unstable and recommends another sync service for phones. On each mobile device, first turn off syncing of the active community plugin list in Sync settings, then make sure the Git plugin is disabled there. Done in the other order, disabling it on the phone syncs back and disables it on the computer too.
6. **Check it.** Create a note, wait ten minutes, and look for it in the repo on GitHub. To push immediately, open the command palette and run "Git: Commit-and-sync". If nothing arrives, run that command and read the error it shows. A plugin that never commits fails silently, so check that a second commit, after your first push, reaches GitHub.
7. **Limit what agents can reach.** When you connect GitHub to Claude or Codex, grant access to selected repositories only.

---

[Previous: Phase 2: Rules and the chief of staff (tier 1)](06-phase-2-rules-and-context.md) | [Contents](../README.md#contents) | [Next: Phase 4: Daily and weekly loops (tier 2)](08-phase-4-daily-and-weekly-loops.md)
