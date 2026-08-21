# Astronaut

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

find / -perm -u=s -type f 2>/dev/null

### Commands used

```bash
find / -perm -u=s -type f 2>/dev/null
```


### References

- https://github.com/CsEnox/CVE-2021-21425/blob/main/exploit.py
- https://gtfobins.github.io/gtfobins/php/#suid

## Evidence

![Pasted image 20240620160039.png](Evidence/Pasted%20image%2020240620160039.png)

![Pasted image 20240620160225.png](Evidence/Pasted%20image%2020240620160225.png)

![Pasted image 20240620160854.png](Internal/Evidence/Pasted%20image%2020240620160854.png)

![Pasted image 20240620160506.png](Internal/Evidence/Pasted%20image%2020240620160506.png)

![Pasted image 20240620160618.png](Internal/Evidence/Pasted%20image%2020240620160618.png)

![Pasted image 20240620160751.png](Internal/Evidence/Pasted%20image%2020240620160751.png)

![Pasted image 20240620160526.png](Internal/Evidence/Pasted%20image%2020240620160526.png)

![Pasted image 20240619232058.png](External/Evidence/Pasted%20image%2020240619232058.png)

![Pasted image 20240619231531.png](External/Evidence/Pasted%20image%2020240619231531.png)
