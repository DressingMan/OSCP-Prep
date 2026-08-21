# Boolean

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
- `33017-http`
- `80-http`

## Attack notes

discovered a root private key in remis .ssh folder tried to ssh into root @ localhost but I got an error after researching the error on stack-overflow I found extra parameters that somehow worked ssh -i root root@127.0.0.1 -o IdentitiesOnly=yes **Lessons learned ->** if you get a "Too many authenication failuers" error use the parameter above or the other one in the link above to stack-overflow

### Commands used

```bash
ssh -i root root@127.0.0.1 -o IdentitiesOnly=yes
```

### References

- _(none)_

## Evidence

![Pasted image 20240716181005.png](Internal/Evidence/Pasted%20image%2020240716181005.png)

![Pasted image 20240716180733.png](Internal/Evidence/Pasted%20image%2020240716180733.png)

![Pasted image 20240716174757.png](Internal/Evidence/Pasted%20image%2020240716174757.png)

![Pasted image 20240716174804.png](Internal/Evidence/Pasted%20image%2020240716174804.png)

![Pasted image 20240716180648.png](Internal/Evidence/Pasted%20image%2020240716180648.png)

![Pasted image 20240716180707.png](Internal/Evidence/Pasted%20image%2020240716180707.png)

![Pasted image 20240716171109.png](External/Evidence/Pasted%20image%2020240716171109.png)

![Pasted image 20240629210813.png](External/Evidence/Pasted%20image%2020240629210813.png)

![Pasted image 20240716170944.png](External/Evidence/Pasted%20image%2020240716170944.png)

![Pasted image 20240716174301.png](External/Evidence/Pasted%20image%2020240716174301.png)

![Pasted image 20240716170628.png](External/Evidence/Pasted%20image%2020240716170628.png)

![Pasted image 20240716174314.png](External/Evidence/Pasted%20image%2020240716174314.png)
