# Phase 5: Phone control and an always-on machine (tier 3)

With a computer that never sleeps, scheduled jobs run on time, cloud output reaches your phone within minutes, and you can start a real agent session from anywhere. Budget a weekend, mostly for networking and testing.

1. **Pick the machine.** A desktop, or a laptop that stays plugged in. Set the OS to never sleep on power, have Obsidian, the agent app and Tailscale launch at login, and leave Obsidian open so the Git plugin keeps committing and pulling.
2. **Join a private network.** Install Tailscale on the computer, phone and tablet with the same account. On the computer, turn on Run unattended, and in Tailscale's admin console disable key expiry for that machine, or it drops off the network after the key expires. Disabling expiry trades some security for uptime, so use Tailscale's access controls to let only your own devices reach this machine.
3. **Steer sessions from your phone (Claude).** Remote Control connects the Claude mobile app to a Claude Code session running on your computer. The code runs locally, and the phone is a window into it. Start it with `/remote-control` in a desktop session, turn on Enable remote control by default in the desktop app's Claude Code settings, or run `claude remote-control --name "My computer"` in a terminal from the vault folder. On the phone, open the Claude app, tap Code, and pick the session. It needs a claude.ai subscription login, and the computer and the session must stay running.
4. **Steer sessions from your phone (Codex).** Codex has its own remote and mobile options. Check its current docs before relying on them.
5. **Keep a repair path.** When the agent session itself is stuck, you need the desktop. On Windows Pro, turn on Remote Desktop and connect over Tailscale with Microsoft's Windows App. Windows Home can't accept Remote Desktop connections. Close the remote window instead of signing out, because signing out ends the session your agents and Obsidian run in. If login is refused with the right password, turn off "only allow Windows Hello sign-in" and use the account password, not the PIN. A password login is only as strong as the password, so make it long and unique, and in Windows Defender Firewall limit the Remote Desktop rule's remote addresses to `100.64.0.0/10`, Tailscale's address range.
6. **Watch for VPN conflicts.** Other VPN clients can block Tailscale traffic, including Remote Desktop connections over it. If a connection fails, pause the other VPN and try again.
7. **Run more than one agent safely.** Never let two agents edit the same folder at once. For code projects, give each agent its own branch in a separate working copy:

```
git worktree add ../project-codex -b codex/task-name
```

For the vault, run one agent at a time. Sync plus two agents editing the same note is how notes get clobbered.

Every folder you expose to phone-started sessions can be read and acted on from your phone. Don't include Downloads or any folder where untrusted files land. A malicious file there can carry instructions aimed at the agent.

---

[Previous: Phase 4: Daily and weekly loops (tier 2)](08-phase-4-daily-and-weekly-loops.md) | [Contents](../README.md#contents) | [Next: Phase 6: Connectors, and how it compounds](10-phase-6-connectors.md)
