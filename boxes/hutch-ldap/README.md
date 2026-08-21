# Hutch (LDAP)

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
- `464-kerberoast`
- `49666-49692-Microsoft-Windows-RPC`
- `53-DNS`
- `593-RPC`
- `5985-Winrm`
- `636-TCPwrapped`
- `80-http`
- `88-kerberos`
- `9389-mc-nmf`
- `UDP-123-ntp`
- `UDP-53-DNS`
- `UDP-88-kerberos`

## Attack notes

_See Exploit.md and Internal/Priv-Esc.md._

### Commands used

_See the phase files._

### References

- _(none)_

## Evidence

![Pasted image 20240715190316.png](External/Evidence/Pasted%20image%2020240715190316.png)

![Pasted image 20240715183916.png](External/Evidence/Pasted%20image%2020240715183916.png)

![Pasted image 20240715185021.png](External/Evidence/Pasted%20image%2020240715185021.png)

![Pasted image 20240715172452.png](External/Evidence/Pasted%20image%2020240715172452.png)

![Pasted image 20240715172933.png](External/Evidence/Pasted%20image%2020240715172933.png)

![Pasted image 20240715185908.png](External/Evidence/Pasted%20image%2020240715185908.png)

![Pasted image 20240715190456.png](External/Evidence/Pasted%20image%2020240715190456.png)
