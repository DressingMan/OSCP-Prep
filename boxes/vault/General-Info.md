## Host Info
```bash
TARGET

64-bit

vault.offsec

```


## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Sat Jul 27 19:16:11 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.056s latency).
Scanned at 2024-07-27 19:16:11 EDT for 543s
Not shown: 988 filtered tcp ports (no-response)
PORT     STATE SERVICE       REASON          VERSION
53/tcp   open  domain?       syn-ack ttl 125
88/tcp   open  kerberos-sec  syn-ack ttl 125 Microsoft Windows Kerberos (server time: 2024-07-27 23:16:22Z)
135/tcp  open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
389/tcp  open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: vault.offsec0., Site: Default-First-Site-Name)
445/tcp  open  microsoft-ds? syn-ack ttl 125
464/tcp  open  kpasswd5?     syn-ack ttl 125
593/tcp  open  ncacn_http    syn-ack ttl 125 Microsoft Windows RPC over HTTP 1.0
636/tcp  open  tcpwrapped    syn-ack ttl 125
3268/tcp open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: vault.offsec0., Site: Default-First-Site-Name)
3269/tcp open  tcpwrapped    syn-ack ttl 125
3389/tcp open  ms-wbt-server syn-ack ttl 125 Microsoft Terminal Services
| ssl-cert: Subject: commonName=DC.vault.offsec
| Issuer: commonName=DC.vault.offsec
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-07-26T23:13:49
| Not valid after:  2025-01-25T23:13:49
| MD5:   106e:78d4:a8c0:6c37:5c07:a958:fad2:59a2
| SHA-1: 4637:7fd7:feca:06ee:a0c9:62ae:364f:44b8:c752:73ab
| -----BEGIN CERTIFICATE-----
| MIIC4jCCAcqgAwIBAgIQGSClrSfTbp1I56XV0VeiAjANBgkqhkiG9w0BAQsFADAa
| MRgwFgYDVQQDEw9EQy52YXVsdC5vZmZzZWMwHhcNMjQwNzI2MjMxMzQ5WhcNMjUw
| MTI1MjMxMzQ5WjAaMRgwFgYDVQQDEw9EQy52YXVsdC5vZmZzZWMwggEiMA0GCSqG
| SIb3DQEBAQUAA4IBDwAwggEKAoIBAQDH/OL02qGg2ssanc1RingsbBkRXj5LCJQK
| 9rNV2iJc5l3CcajEzxb6ObnapZWAV9tcfpWDnKrKQGCNBx0V5XSe/rou/Wf7VIkp
| 3RQiQyeokWNI3Cz/iuhQDbiHaxq01CUiPsvppIECX0MJO9RDf5sXbttMl2gBFY4m
| 1OAuYufPj37FqplGSUm6WxghOMlmjMs461cHwCOB6jJtSp3+D2aj3CXn+q5Nkg6E
| ntXHaUyDspnBc9IJqdbMu21q2KGM3UTz3PqCB0B6yoa+WtJ5PhqL9c/W087hGAjA
| eAxBOSbaa1oaslOzirAvjGDyxDtBvpxcSkUDGDwo9JNWUuci+ZGtAgMBAAGjJDAi
| MBMGA1UdJQQMMAoGCCsGAQUFBwMBMAsGA1UdDwQEAwIEMDANBgkqhkiG9w0BAQsF
| AAOCAQEAWyZBaArInss3pzYphmxQSQEWgQsgcX0ho/tXETqVQfjQPJvMbgq5Iidu
| c+aPABapp+UySQtC7R0a2kNHIjmDuY/VcKTW+Y6Lnhl6Z+gkN3pF4lPZuswKYBAu
| JRpAlnzrnPX+d1AUEBXoXUtQ802Tw/E6MvIVeh2/y4GxLjPEfT677oVshEYeBaNY
| eueqwfQiue4bOwp1dv+jMF/OBGLZogOhzj6yW2v15VZAqQLqAwUV+7vSlcRMTlog
| 2fMjViovdqwSySQQYXZwF7o8y3WhzkQKSQNu+wMYk9rvnzBJhAb09SRDtLSIN7Dy
| P+eiNJrehxGKGSCqLwnxk5dVUo19/g==
|_-----END CERTIFICATE-----
|_ssl-date: 2024-07-27T23:25:12+00:00; 0s from scanner time.
| rdp-ntlm-info: 
|   Target_Name: VAULT
|   NetBIOS_Domain_Name: VAULT
|   NetBIOS_Computer_Name: DC
|   DNS_Domain_Name: vault.offsec
|   DNS_Computer_Name: DC.vault.offsec
|   DNS_Tree_Name: vault.offsec
|   Product_Version: 10.0.17763
|_  System_Time: 2024-07-27T23:24:32+00:00
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
No OS matches for host
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=7/27%OT=53%CT=%CU=%PV=Y%DS=4%DC=T%G=N%TM=66A581DA%P=x86_64-pc-linux-gnu)
SEQ(SP=106%GCD=1%ISR=10B%TI=I%TS=U)
OPS(O1=M551NW8NNS%O2=M551NW8NNS%O3=M551NW8%O4=M551NW8NNS%O5=M551NW8NNS%O6=M551NNS)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)
ECN(R=Y%DF=Y%TG=80%W=FFFF%O=M551NW8NNS%CC=Y%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
U1(R=N)
IE(R=N)

Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=262 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: Host: DC; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 29728/tcp): CLEAN (Timeout)
|   Check 2 (port 53840/tcp): CLEAN (Timeout)
|   Check 3 (port 22960/udp): CLEAN (Timeout)
|   Check 4 (port 45210/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
|_clock-skew: mean: 0s, deviation: 0s, median: 0s
| smb2-time: 
|   date: 2024-07-27T23:24:34
|_  start_date: N/A
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required

TRACEROUTE (using port 139/tcp)
HOP RTT      ADDRESS
1   53.82 ms ATTACKER
2   53.81 ms ATTACKER
3   54.45 ms TARGET
4   55.10 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Jul 27 19:25:14 2024 -- 1 IP address (1 host up) scanned in 543.51 seconds

```

#### Full Scan
```bash

# Nmap 7.94SVN scan initiated Sat Jul 27 19:16:11 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.056s latency).
Scanned at 2024-07-27 19:16:11 EDT for 208s
Not shown: 65514 filtered tcp ports (no-response)
PORT      STATE SERVICE       REASON          VERSION
53/tcp    open  domain        syn-ack ttl 125 Simple DNS Plus
88/tcp    open  kerberos-sec  syn-ack ttl 125 Microsoft Windows Kerberos (server time: 2024-07-27 23:17:56Z)
135/tcp   open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
389/tcp   open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: vault.offsec0., Site: Default-First-Site-Name)
445/tcp   open  microsoft-ds? syn-ack ttl 125
464/tcp   open  kpasswd5?     syn-ack ttl 125
593/tcp   open  ncacn_http    syn-ack ttl 125 Microsoft Windows RPC over HTTP 1.0
636/tcp   open  tcpwrapped    syn-ack ttl 125
3268/tcp  open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: vault.offsec0., Site: Default-First-Site-Name)
3269/tcp  open  tcpwrapped    syn-ack ttl 125
3389/tcp  open  ms-wbt-server syn-ack ttl 125 Microsoft Terminal Services
|_ssl-date: 2024-07-27T23:19:37+00:00; 0s from scanner time.
| ssl-cert: Subject: commonName=DC.vault.offsec
| Issuer: commonName=DC.vault.offsec
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-07-26T23:13:49
| Not valid after:  2025-01-25T23:13:49
| MD5:   106e:78d4:a8c0:6c37:5c07:a958:fad2:59a2
| SHA-1: 4637:7fd7:feca:06ee:a0c9:62ae:364f:44b8:c752:73ab
| -----BEGIN CERTIFICATE-----
| MIIC4jCCAcqgAwIBAgIQGSClrSfTbp1I56XV0VeiAjANBgkqhkiG9w0BAQsFADAa
| MRgwFgYDVQQDEw9EQy52YXVsdC5vZmZzZWMwHhcNMjQwNzI2MjMxMzQ5WhcNMjUw
| MTI1MjMxMzQ5WjAaMRgwFgYDVQQDEw9EQy52YXVsdC5vZmZzZWMwggEiMA0GCSqG
| SIb3DQEBAQUAA4IBDwAwggEKAoIBAQDH/OL02qGg2ssanc1RingsbBkRXj5LCJQK
| 9rNV2iJc5l3CcajEzxb6ObnapZWAV9tcfpWDnKrKQGCNBx0V5XSe/rou/Wf7VIkp
| 3RQiQyeokWNI3Cz/iuhQDbiHaxq01CUiPsvppIECX0MJO9RDf5sXbttMl2gBFY4m
| 1OAuYufPj37FqplGSUm6WxghOMlmjMs461cHwCOB6jJtSp3+D2aj3CXn+q5Nkg6E
| ntXHaUyDspnBc9IJqdbMu21q2KGM3UTz3PqCB0B6yoa+WtJ5PhqL9c/W087hGAjA
| eAxBOSbaa1oaslOzirAvjGDyxDtBvpxcSkUDGDwo9JNWUuci+ZGtAgMBAAGjJDAi
| MBMGA1UdJQQMMAoGCCsGAQUFBwMBMAsGA1UdDwQEAwIEMDANBgkqhkiG9w0BAQsF
| AAOCAQEAWyZBaArInss3pzYphmxQSQEWgQsgcX0ho/tXETqVQfjQPJvMbgq5Iidu
| c+aPABapp+UySQtC7R0a2kNHIjmDuY/VcKTW+Y6Lnhl6Z+gkN3pF4lPZuswKYBAu
| JRpAlnzrnPX+d1AUEBXoXUtQ802Tw/E6MvIVeh2/y4GxLjPEfT677oVshEYeBaNY
| eueqwfQiue4bOwp1dv+jMF/OBGLZogOhzj6yW2v15VZAqQLqAwUV+7vSlcRMTlog
| 2fMjViovdqwSySQQYXZwF7o8y3WhzkQKSQNu+wMYk9rvnzBJhAb09SRDtLSIN7Dy
| P+eiNJrehxGKGSCqLwnxk5dVUo19/g==
|_-----END CERTIFICATE-----
| rdp-ntlm-info: 
|   Target_Name: VAULT
|   NetBIOS_Domain_Name: VAULT
|   NetBIOS_Computer_Name: DC
|   DNS_Domain_Name: vault.offsec
|   DNS_Computer_Name: DC.vault.offsec
|   DNS_Tree_Name: vault.offsec
|   Product_Version: 10.0.17763
|_  System_Time: 2024-07-27T23:18:57+00:00
5985/tcp  open  http          syn-ack ttl 125 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
9389/tcp  open  mc-nmf        syn-ack ttl 125 .NET Message Framing
49666/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49667/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49673/tcp open  ncacn_http    syn-ack ttl 125 Microsoft Windows RPC over HTTP 1.0
49674/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49679/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49706/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49826/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
No OS matches for host
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=7/27%OT=53%CT=%CU=%PV=Y%DS=4%DC=T%G=N%TM=66A5808B%P=x86_64-pc-linux-gnu)
SEQ(SP=106%GCD=1%ISR=108%TI=I%TS=U)
SEQ(SP=FD%GCD=1%ISR=FF%TI=I%TS=U)
OPS(O1=M551NW8NNS%O2=M551NW8NNS%O3=M551NW8%O4=M551NW8NNS%O5=M551NW8NNS%O6=M551NNS)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)
ECN(R=Y%DF=Y%TG=80%W=FFFF%O=M551NW8NNS%CC=Y%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
U1(R=N)
IE(R=N)

Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=253 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: Host: DC; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required
|_clock-skew: mean: 0s, deviation: 0s, median: 0s
| smb2-time: 
|   date: 2024-07-27T23:18:59
|_  start_date: N/A
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 29728/tcp): CLEAN (Timeout)
|   Check 2 (port 53840/tcp): CLEAN (Timeout)
|   Check 3 (port 22960/udp): CLEAN (Timeout)
|   Check 4 (port 45210/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked

TRACEROUTE (using port 135/tcp)
HOP RTT      ADDRESS
1   54.46 ms ATTACKER
2   54.44 ms ATTACKER
3   55.78 ms TARGET
4   56.05 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Jul 27 19:19:39 2024 -- 1 IP address (1 host up) scanned in 208.04 seconds

```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Sat Jul 27 19:16:11 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-07-27 19:16:12 EDT for 1776s
Not shown: 97 open|filtered udp ports (no-response)
PORT    STATE SERVICE      REASON               VERSION
53/udp  open  domain       udp-response ttl 125 (generic dns response: NOTIMP)
| fingerprint-strings: 
|   NBTStat: 
|_    CKAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
88/udp  open  kerberos-sec udp-response ttl 125 Microsoft Windows Kerberos (server time: 2024-07-27 23:16:11Z)
123/udp open  ntp          udp-response ttl 125 NTP v3
| ntp-info: 
|_  receive time stamp: 2024-07-27T23:23:12
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port53-UDP:V=7.94SVN%I=7%D=7/27%Time=66A57FCD%P=x86_64-pc-linux-gnu%r(N
SF:BTStat,32,"\x80\xf0\x80\x82\0\x01\0\0\0\0\0\0\x20CKAAAAAAAAAAAAAAAAAAAA
SF:AAAAAAAAAA\0\0!\0\x01");
Too many fingerprints match this host to give specific OS details
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=7/27%OT=%CT=%CU=%PV=Y%G=N%TM=66A586AC%P=x86_64-pc-linux-gnu)
SEQ()
U1(R=N)
IE(R=N)

Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: 7s

TRACEROUTE (using port 88/udp)
HOP RTT      ADDRESS
1   52.62 ms ATTACKER
2   52.60 ms ATTACKER
3   54.17 ms TARGET
4   ... 30

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Jul 27 19:45:48 2024 -- 1 IP address (1 host up) scanned in 1777.69 seconds


```

