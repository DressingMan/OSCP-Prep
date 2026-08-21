# Twiggy

Sanitized practice-box notes. Folder layout matches the Obsidian template: **General Info → External (per port) → Exploit → Internal / Priv Esc → Loot**, with **Evidence** next to the phase where the screenshot was taken.

| | |
| --- | --- |
| OS (guess from ports) | Linux |
| Notes | Personal walkthrough, not a spoiler-free writeup |

## Layout

- [General Info](General-Info.md)
- [Exploit](Exploit.md)
- [Loot](Loot.md)
- [External](External/) — per-port enumeration
- [Internal / Priv Esc](Internal/Priv-Esc.md)

### Ports touched

- `22-ssh`
- `4505-zmtp`
- `4506-zmtp`
- `53-DNS`
- `80-http`
- `8000-http`

## Attack notes

_See Exploit.md and Internal/Priv-Esc.md._

### Commands used

_See the phase files._

### References

- https://github.com/Al1ex/CVE-2020-11652/blob/main/CVE-2020-11652.py

## Evidence

![Pasted image 20240629174736.png](Evidence/Pasted%20image%2020240629174736.png)

![Pasted image 20240629164906.png](External/Evidence/Pasted%20image%2020240629164906.png)

![Pasted image 20240629164634.png](External/Evidence/Pasted%20image%2020240629164634.png)

![Pasted image 20240629170003.png](External/Evidence/Pasted%20image%2020240629170003.png)
