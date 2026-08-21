# RubyDome

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
- `3000-http`

## Attack notes

POST parameter = url the URL needs to be http://$IP:3000/pdf

### Commands used

```bash
echo 'system("chmod +s /usr/bin/bash")' > app.rb
```


### References

- https://github.com/UNICORDev/exploit-CVE-2022-25765

## Evidence

![Pasted image 20240712160108.png](Evidence/Pasted%20image%2020240712160108.png)

![Pasted image 20240712160222.png](Evidence/Pasted%20image%2020240712160222.png)

![Pasted image 20240712155048.png](Evidence/Pasted%20image%2020240712155048.png)

![Pasted image 20240712160210.png](Evidence/Pasted%20image%2020240712160210.png)

![Pasted image 20240712160534.png](Internal/Evidence/Pasted%20image%2020240712160534.png)

![Pasted image 20240712160734.png](Internal/Evidence/Pasted%20image%2020240712160734.png)

![Pasted image 20240712163458.png](Internal/Evidence/Pasted%20image%2020240712163458.png)

![Pasted image 20240712160757.png](Internal/Evidence/Pasted%20image%2020240712160757.png)

![Pasted image 20240712163542.png](Internal/Evidence/Pasted%20image%2020240712163542.png)

![Pasted image 20240712153905.png](External/Evidence/Pasted%20image%2020240712153905.png)

![Pasted image 20240712155031.png](External/Evidence/Pasted%20image%2020240712155031.png)
