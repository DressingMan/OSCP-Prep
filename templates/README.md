# Templates

Copy these when you start a box. Headings stay empty until that phase of the machine produces notes.

## Box skeleton (`box/`)

| File | Use |
| --- | --- |
| [General-Info.md](box/General-Info.md) | Host, OS, users |
| [Pentest-Header.md](box/Pentest-Header.md) | Full engagement dump: nmap, web, priv-esc, takeaways |
| [Exploit.md](box/Exploit.md) | Foothold / PoC / listener |
| [Priv-Esc.md](box/Priv-Esc.md) | Internal escalation |
| [Loot.md](box/Loot.md) | Users, passwords, hashes |

## Ports (`ports/`)

One file per listening service. Same names I use in writeups (`80-http`, `445-SMB`, `22-ssh`, …).

Placeholders in commands: `$IP` / `TARGET` for the victim, `ATTACKER` for Kali.
