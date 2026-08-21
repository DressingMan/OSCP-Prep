# Templates

Copy these when you start a box. Headings stay empty until that phase produces notes.

## Box skeleton (`box/`)

Copy the whole folder into `boxes/<machine>/`.

| File | Use |
| --- | --- |
| [General-Info.md](box/General-Info.md) | Host, OS, nmap (short port table) |
| [Pentest-Header.md](box/Pentest-Header.md) | Engagement dump: users, creds, to-try, takeaways |
| [Exploit.md](box/Exploit.md) | Foothold / PoC / listener |
| [Priv-Esc.md](box/Priv-Esc.md) | Internal escalation (move under `Internal/` on a real box) |
| [Loot.md](box/Loot.md) | Users, passwords, hashes |

## Ports (`ports/`)

One file per listening service. Copy into `External/` and keep the same names as the writeups (`80-http`, `445-SMB`, `22-ssh`, …).

Placeholders: `$IP` / `TARGET` for the victim, `ATTACKER` for Kali.

Repo overview and the full “new box” workflow: [README](../README.md#structure-your-own-notes).
