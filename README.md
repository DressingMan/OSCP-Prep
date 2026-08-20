# OSCP Prep

Personal pentest notes from OSCP-style practice: how I template a box, which tools I reach for, and sanitized writeups of six completed TJ Null list machines.

This is **my** workflow, not OffSec course material. Exam notes and lab-only machines are not in this repo.

Lab IPs in text are replaced with `TARGET` (victim) and `ATTACKER` (Kali). Screenshots are original practice captures and may still show isolated lab addresses.

## Layout

| Path | What it is |
| --- | --- |
| [`templates/`](templates/) | Box skeleton + per-port note templates |
| [`tools/`](tools/) | Command cheatsheets |
| [`methodology/`](methodology/) | Enumeration, priv-esc, AD, file transfer, shells |
| [`boxes/`](boxes/) | Six completed practice boxes (with screenshots) |

## Boxes (v1)

| Box | Notes |
| --- | --- |
| [Crane](boxes/crane/) | Linux, SuiteCRM, CVE-2022-23940 |
| [Flu](boxes/flu/) | Linux, extra HTTP services |
| [law](boxes/law/) | Linux, web CVE (GLPI / CVE-2022-35914) |
| [PC](boxes/pc/) | Linux, HTTP on 8000 |
| [Pelican](boxes/pelican/) | Linux, busy surface (SMB, CUPS, RMI, extra SSH) |
| [Press](boxes/press/) | Linux, HTTP + extra port |

Each box follows the same tree: `General-Info` → `External/<port>` → `Exploit` → `Internal/Priv-Esc` → `Loot`, plus `Evidence/` screenshots.

## How I use the templates

1. Copy `templates/box/` into a new folder named after the machine.
2. Drop a note under `External/` for every interesting port (copy from `templates/ports/`).
3. Keep loot, exploit path, and takeaways in the matching files as I go.

## Disclaimer

For education and authorized testing only. Do not use these techniques against systems you do not own or do not have permission to test.

More writeups (retired vault) will be added after this first set looks right.
