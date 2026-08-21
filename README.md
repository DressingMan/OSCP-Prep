# OSCP Prep

Personal pentest notes: a **repeatable box layout**, **port/tool cheatsheets**, and **sanitized practice writeups**.

Lab IPs in **text** are `TARGET` (victim) and `ATTACKER` (Kali). Screenshots are original practice captures and may still show isolated lab addresses.

## What’s in the repo

| Path | What it is |
| --- | --- |
| [templates/](templates/) | Blank skeleton you copy for every new machine |
| [tools/](tools/) | Command snippets (nmap, netexec, gobuster, hashcat, …) |
| [methodology/](methodology/) | Broader workflow: enum, priv-esc, AD, shells, file transfer |
| [boxes/](boxes/) | Completed practice machines using that skeleton |
| [setup/](setup/) | How this notes environment is set up (Sublime + Obsidian) |

**Start here depending on what you want:**

| I want to… | Go to |
| --- | --- |
| See how a finished box is documented | [boxes/](boxes/) → pick a machine → its `README.md` |
| Start notes on a **new** machine | [How to structure your own notes](#structure-your-own-notes) |
| Look up a command | [tools/](tools/) then [methodology/](methodology/) if you need the “when” |
| Match the editor / screenshot setup | [setup/sublime-and-obsidian.md](setup/sublime-and-obsidian.md) |

## How to browse

1. **Index** — [boxes/README.md](boxes/README.md) lists every machine (Linux vs Windows/AD).
2. **Box landing page** — each folder has a `README.md`: short path, ports, commands, evidence.
3. **Same tree every time** — read in this order:

```
README.md          ← high-level path (read this first)
General-Info.md    ← host + nmap (kept short)
External/          ← one file per open port
Exploit.md         ← foothold
Internal/Priv-Esc.md
Loot.md            ← users / creds / hashes
evidence/          ← screenshots next to the phase they belong to
```

4. **Tools** — [tools/README.md](tools/README.md) is an A–Z of cheatsheets. Files are copy-paste commands, not tutorials.
5. **Templates** — [templates/](templates/) are the empty versions of the files under `boxes/`.

Example: [Crane](boxes/crane/) (Linux web) or [Access](boxes/access/) (Windows / AD).

## Templates to use

Copy from [`templates/box/`](templates/box/) when you spawn a machine:

| File | Fill this in |
| --- | --- |
| [General-Info.md](templates/box/General-Info.md) | Host, OS, nmap (port table only — not the full dump) |
| [Pentest-Header.md](templates/box/Pentest-Header.md) | One-pager: users, creds, to-try list, takeaways |
| [Exploit.md](templates/box/Exploit.md) | PoC, listener, foothold |
| [Priv-Esc.md](templates/box/Priv-Esc.md) | Internal escalation |
| [Loot.md](templates/box/Loot.md) | Users, passwords, hashes |

Then copy **one port file** from [`templates/ports/`](templates/ports/) into `External/` for each listening service (`80-http`, `445-SMB`, `22-ssh`, …).

Placeholders: `TARGET` / `$IP` = victim, `ATTACKER` = your box.

## Structure your own notes

```text
boxes/<machine-name>/
  README.md                 ← write last: 5–10 line path
  General-Info.md
  Exploit.md
  Loot.md
  External/
    22-ssh.md
    80-http.md
    445-SMB.md
    evidence/               ← paste screenshots here
  Internal/
    Priv-Esc.md
    evidence/
```

**While you attack**

1. Create `boxes/<name>/` and copy `templates/box/*` in.
2. Drop nmap into `General-Info.md` (open ports + versions only).
3. For each interesting port, copy the matching file from `templates/ports/` into `External/`.
4. Paste screenshots as you go (Obsidian → `evidence/` subfolder).
5. Keep foothold in `Exploit.md`, loot in `Loot.md`, escalation in `Internal/Priv-Esc.md`.
6. When the box is done, write `README.md`: OS, foothold, privesc, 3–5 commands.

**Conventions**

- One box = one folder. Don’t mix machines.
- One port = one note. Don’t dump the whole scan into `80-http.md`.
- Commands in fenced blocks so they’re greppable later (and so they can move into `tools/`).
- When a command is reusable, copy it into `tools/<tool>.md` instead of burying it in a writeup.

## Editor setup

Sublime for config/scripts, Obsidian for the vault and screenshots: **[setup/sublime-and-obsidian.md](setup/sublime-and-obsidian.md)**.

## License

[MIT](LICENSE) © 2026 PassTh3H4sh

## Disclaimer

For education and authorized testing only. Do not use these techniques against systems you do not own or do not have permission to test.
