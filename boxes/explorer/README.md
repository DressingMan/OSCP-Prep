# Explorer

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
- `80-http`

## Attack notes

upgrade shell to a tty dora is in the disk group with `debugfs` we can read files with root permissions we can read the entire /etc/shadow file containing roots hashed password we cracked roots password with john now we can su aka switch user to root

### Commands used

_See the phase files._

### References

- _(none)_

## Evidence

![Pasted image 20240712143116.png](Internal/Evidence/Pasted%20image%2020240712143116.png)

![Pasted image 20240712145808.png](Internal/Evidence/Pasted%20image%2020240712145808.png)

![Pasted image 20240712145616.png](Internal/Evidence/Pasted%20image%2020240712145616.png)

![Pasted image 20240712150445.png](Internal/Evidence/Pasted%20image%2020240712150445.png)

![Pasted image 20240712150644.png](Internal/Evidence/Pasted%20image%2020240712150644.png)

![Pasted image 20240712145856.png](Internal/Evidence/Pasted%20image%2020240712145856.png)

![Pasted image 20240712150715.png](Internal/Evidence/Pasted%20image%2020240712150715.png)

![Pasted image 20240712150313.png](Internal/Evidence/Pasted%20image%2020240712150313.png)

![Pasted image 20240712150558.png](Internal/Evidence/Pasted%20image%2020240712150558.png)

![Pasted image 20240712142356.png](External/Evidence/Pasted%20image%2020240712142356.png)

![Pasted image 20240712141922.png](External/Evidence/Pasted%20image%2020240712141922.png)

![Pasted image 20240712141739.png](External/Evidence/Pasted%20image%2020240712141739.png)
