# Phase 3: History on GitHub (tier 2)

Git can restore snapshots of tracked content that you commit. GitHub stores the commits you push and can provide a copy for configured cloud jobs. Neither captures every edit between commits. Do this before you let any job run unattended. About 30 minutes.

1. **Install Git and the GitHub CLI.** Windows: `winget install --id Git.Git` and `winget install --id GitHub.cli`. Mac: install Git from git-scm.com and the CLI from cli.github.com. Close and reopen the terminal afterwards so it finds the new commands.
2. **Sign in once.**

```
gh auth login
```

In `gh auth login`, choose GitHub.com, HTTPS and browser login. That also sets up Git's credentials. Your noreply address is under GitHub Settings, Emails. Use it with your GitHub handle as the author name if you want a pseudonymous public identity. Set the repository-specific identity after git init below.

3. **Put the vault in a private repo.** From inside the vault folder:

```
git init -b main
git config user.name "Your GitHub handle"
git config user.email "your-id@users.noreply.github.com"
```

Then create the `.gitignore`, unless you used the starter vault, which already has one. PowerShell:

```
Set-Content .gitignore -Value ".obsidian/workspace.json", ".obsidian/workspace-mobile.json", ".trash/", ".env", ".env.*"
```

Mac or Linux:

```
printf '%s\n' .obsidian/workspace.json .obsidian/workspace-mobile.json .trash/ .env ".env.*" > .gitignore
```

Then commit and push:

```
git add -A
git diff --cached --stat
git diff --cached
git commit -m "Initial vault"
gh repo create my-vault --private --source . --remote origin --push
```

The last command prints the new repo's URL. The ignore list excludes window layouts, trash and environment files. Review the staged diff before committing. Ignore rules do not remove files or secrets already in history.

4. **Auto-commit from the desktop.** In Obsidian on the computer: Settings, Community plugins, turn them on, Browse, install and enable **Git** by Vinzent03. Set the automatic commit-and-sync interval to 10 minutes and turn on pull on startup. If you enabled the plugin before the folder was a repo, restart Obsidian.
5. **Keep Git off your phone and tablet.** The plugin's author calls its mobile version very unstable and recommends another sync service for phones. On each mobile device, first turn off syncing of the active community plugin list in Sync settings, then make sure the Git plugin is disabled there. Done in the other order, disabling it on the phone syncs back and disables it on the computer too.
6. **Check it.** Create a note, wait ten minutes, and look for it in the repo on GitHub. To push immediately, open the command palette and run "Git: Commit-and-sync". If nothing arrives, run that command and read the error it shows. Confirm a second automatic commit after your first push. Then change a disposable test note and restore its earlier committed content, keeping unrelated changes. Commit before consequential work if you need an immediate recovery point. The configured interval is not a guarantee that every edit was captured.
7. **Limit what agents can reach.** When you connect GitHub to Claude or Codex, grant access to selected repositories only.

---

[Previous: Phase 2: Rules and the chief of staff (tier 1)](06-phase-2-rules-and-context.md) | [Contents](../README.md#contents) | [Next: Phase 4: Daily and weekly loops (tier 2)](08-phase-4-daily-and-weekly-loops.md)
