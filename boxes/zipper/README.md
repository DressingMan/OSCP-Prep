# Zipper

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

upgraded shell to a valid TTY creating a symbolic link to connect  /root/secret to enox.zip-> ln -s /root/secret enox.zip Next we create a file named @enox.zip which will tell 7z that enox.zip is a list file: password revealed = WildCardsGoingWild

### Commands used

```bash
ln -s /root/secret enox.zip
touch @enox.zip
```


### References

- _(none)_

## Evidence

![Pasted image 20240716163447.png](Internal/Evidence/Pasted%20image%2020240716163447.png)

![Pasted image 20240716161734.png](Internal/Evidence/Pasted%20image%2020240716161734.png)

![Pasted image 20240716163624.png](Internal/Evidence/Pasted%20image%2020240716163624.png)

![Pasted image 20240716161809.png](Internal/Evidence/Pasted%20image%2020240716161809.png)

![Pasted image 20240716161612.png](Internal/Evidence/Pasted%20image%2020240716161612.png)

![Pasted image 20240716161245.png](External/Evidence/Pasted%20image%2020240716161245.png)

![Pasted image 20240716152317.png](External/Evidence/Pasted%20image%2020240716152317.png)

![Pasted image 20240716152613.png](External/Evidence/Pasted%20image%2020240716152613.png)

![Pasted image 20240716152823.png](External/Evidence/Pasted%20image%2020240716152823.png)

![Pasted image 20240716154525.png](External/Evidence/Pasted%20image%2020240716154525.png)

![Pasted image 20240716151114.png](External/Evidence/Pasted%20image%2020240716151114.png)

![Pasted image 20240716152440.png](External/Evidence/Pasted%20image%2020240716152440.png)
