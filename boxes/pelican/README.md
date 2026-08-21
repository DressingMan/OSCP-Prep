# Pelican

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

- `139-netbios-ssn`
- `22-ssh`
- `2222-ssh`
- `44267-JAVA-RMI`
- `445-SMB`
- `5353-DNS-UDP`
- `631-CUPS`
- `8080-http`
- `8081-http`

## Attack notes

_See Exploit.md and Internal/Priv-Esc.md._

### Commands used

_See the phase files._

### References

- https://www.exploit-db.com/exploits/48654

## Evidence

![Pasted image 20241017162055.png](Evidence/Pasted%20image%2020241017162055.png)

![Pasted image 20241017162105.png](Evidence/Pasted%20image%2020241017162105.png)

![Pasted image 20241017162902.png](Internal/Evidence/Pasted%20image%2020241017162902.png)

![Pasted image 20241017162536.png](Internal/Evidence/Pasted%20image%2020241017162536.png)

![Pasted image 20241017163041.png](Internal/Evidence/Pasted%20image%2020241017163041.png)

![Pasted image 20241017163333.png](Internal/Evidence/Pasted%20image%2020241017163333.png)

![Pasted image 20241017163230.png](Internal/Evidence/Pasted%20image%2020241017163230.png)

![Pasted image 20241017160351.png](External/Evidence/Pasted%20image%2020241017160351.png)

![Pasted image 20241017160553.png](External/Evidence/Pasted%20image%2020241017160553.png)
