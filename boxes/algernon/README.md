# Algernon

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
- `17001-remoting`
- `21-FTP`
- `49664-55885-Microsoft-Windows-RPC`
- `80-http`
- `9998-http`

## Attack notes

We have a RCE the build version doesn't match, but I might get lucky! I had to modify the weaponized code to match my target machine and my local machine by changing the IP address and Port. I set up my listener on 4444 with netcat aka (nc) to catch the reverse shell -> running the exploit ->

### Commands used

```bash
nc -nlvp 4444
python3 49216.py
```

### References

- https://www.exploit-db.com/exploits/49216

## Evidence

![Pasted image 20240625001907.png](Evidence/Pasted%20image%2020240625001907.png)

![Pasted image 20240624234658.png](Evidence/Pasted%20image%2020240624234658.png)

![Pasted image 20240625002042.png](Evidence/Pasted%20image%2020240625002042.png)

![Pasted image 20240625002242.png](Evidence/Pasted%20image%2020240625002242.png)

![Pasted image 20240625002435.png](Evidence/Pasted%20image%2020240625002435.png)

![Pasted image 20240624234541.png](External/Evidence/Pasted%20image%2020240624234541.png)

![Pasted image 20240624232250.png](External/Evidence/Pasted%20image%2020240624232250.png)

![Pasted image 20240624231930.png](External/Evidence/Pasted%20image%2020240624231930.png)

![Pasted image 20240624232032.png](External/Evidence/Pasted%20image%2020240624232032.png)

![Pasted image 20240624232556.png](External/Evidence/Pasted%20image%2020240624232556.png)

![Pasted image 20240624232348.png](External/Evidence/Pasted%20image%2020240624232348.png)

![Pasted image 20240624233907.png](External/Evidence/Pasted%20image%2020240624233907.png)
