## Host Info
```
Service Info: Host: DC01; OS: Windows; CPE: 

DNS name = heist.offsec

rootDomainNamingContext: DC=heist,DC=offsec

TARGET

```


## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Wed Jun 19 19:02:26 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -204746 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -204746 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -191269 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -191269 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.060s latency).
Scanned at 2024-06-19 19:02:27 EDT for 545s
Not shown: 987 filtered tcp ports (no-response)
PORT     STATE SERVICE       REASON          VERSION
53/tcp   open  domain?       syn-ack ttl 125
88/tcp   open  kerberos-sec  syn-ack ttl 125 Microsoft Windows Kerberos (server time: 2024-06-19 23:02:38Z)
135/tcp  open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
389/tcp  open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: heist.offsec0., Site: Default-First-Site-Name)
445/tcp  open  microsoft-ds? syn-ack ttl 125
464/tcp  open  kpasswd5?     syn-ack ttl 125
593/tcp  open  ncacn_http    syn-ack ttl 125 Microsoft Windows RPC over HTTP 1.0
636/tcp  open  tcpwrapped    syn-ack ttl 125
3268/tcp open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: heist.offsec0., Site: Default-First-Site-Name)
3269/tcp open  tcpwrapped    syn-ack ttl 125
3389/tcp open  ms-wbt-server syn-ack ttl 125 Microsoft Terminal Services
| rdp-ntlm-info: 
|   Target_Name: HEIST
|   NetBIOS_Domain_Name: HEIST
|   NetBIOS_Computer_Name: DC01
|   DNS_Domain_Name: heist.offsec
|   DNS_Computer_Name: DC01.heist.offsec
|   DNS_Tree_Name: heist.offsec
|   Product_Version: 10.0.17763
|_  System_Time: 2024-06-19T23:10:50+00:00
|_ssl-date: 2024-06-19T23:11:30+00:00; +1s from scanner time.
| ssl-cert: Subject: commonName=DC01.heist.offsec
| Issuer: commonName=DC01.heist.offsec
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-06-18T23:00:58
| Not valid after:  2024-12-18T23:00:58
| MD5:   6f7f:333b:d462:cbe8:0df1:1536:9bcf:fed5
| SHA-1: a327:0056:3b82:99af:9100:a348:985b:7f9b:88f8:ab22
| -----BEGIN CERTIFICATE-----
| MIIC5jCCAc6gAwIBAgIQXn4vqQ62UK5Dcpm6JoAr+TANBgkqhkiG9w0BAQsFADAc
| MRowGAYDVQQDExFEQzAxLmhlaXN0Lm9mZnNlYzAeFw0yNDA2MTgyMzAwNThaFw0y
| NDEyMTgyMzAwNThaMBwxGjAYBgNVBAMTEURDMDEuaGVpc3Qub2Zmc2VjMIIBIjAN
| BgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAs8sIVBQ+kyaS9rsGgLCEo/vTIGiu
| QXQu2CA2GBW0Ew87d+fwRWHC3Y2ELEqfQAbiaE2X2yKZlCDVPoS6eEuGfCqldZs0
| DqZU1XZifLH1xPEPihmY+gvf5PBWNYmMFUR/SS76HQuSypuDs5fCICVYjZJzgG8a
| no0oO5zHL5dOJZTM91adFFC+pkkf1p3cah8pk/PkkFZpEQkvc+osicDdSFs+oIPc
| JBFbeuvEqttjY5i6n2xBjal7A6uHsrod2dn4z21pQtZxsJfV1hit1/7QGRNq6XcS
| I5hCnCxXPCnEmjbSgJkVcccdWkW9brvNVyg56gocsXTWEY1L+fNXb1S58QIDAQAB
| oyQwIjATBgNVHSUEDDAKBggrBgEFBQcDATALBgNVHQ8EBAMCBDAwDQYJKoZIhvcN
| AQELBQADggEBAEqpSvlVWaQ0mdidfr5Lv+MoQVsFr0MohN1p1n4SGSURNskTgPXK
| agLHDdseoxxwAAjIk82Bv2HbVnEboZHLEqS1tGpgRKS16vg/0WhOR6YMhM2slB/g
| LfyV2GF6eLNHEYRboHF5g30v/BBGm+wQ7E8cCGFJB+ARXYcWjKkAfZauamQx0UIY
| N9cpHHm9bhxZfeqV7JvcfpkCyYnO+HTPdGIynqY6PRWvx4HNm4Y7erSFGVwYjJiV
| Cl6MP7HD1VUWho4jmslFYSKqbyXoWYssbQdZ0pJwYgG91/71tvqH4GVRITinT5n5
| a1qzzCmXqmPY+OdZTjbX1aoDHsWOgsbJcxY=
|_-----END CERTIFICATE-----
8080/tcp open  http          syn-ack ttl 125 Werkzeug httpd 2.0.1 (Python 3.9.0)
| http-methods: 
|_  Supported Methods: OPTIONS GET HEAD
|_http-server-header: Werkzeug/2.0.1 Python/3.9.0
|_http-title: Super Secure Web Browser
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows XP (86%)
OS CPE: cpe:/o:microsoft:windows_xp::sp3
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
Aggressive OS guesses: Microsoft Windows XP SP3 (86%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=6/19%OT=53%CT=%CU=%PV=Y%DS=4%DC=T%G=N%TM=667365A4%P=x86_64-pc-linux-gnu)
SEQ(SP=100%GCD=1%ISR=108%TS=U)
SEQ(SP=100%GCD=2%ISR=108%TS=U)
OPS(O1=M551NW8NNS%O2=M551NW8NNS%O3=M551NW8%O4=M551NW8NNS%O5=M551NW8NNS%O6=M551NNS)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)
ECN(R=Y%DF=Y%TG=80%W=FFFF%O=M551NW8NNS%CC=Y%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T3(R=Y%DF=Y%TG=80%W=FFFF%S=O%A=O%F=AS%O=M551NW8NNS%RD=0%Q=)
T4(R=N)
U1(R=N)
IE(R=N)

Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=256 (Good luck!)
IP ID Sequence Generation: Busy server or unknown class
Service Info: Host: DC01; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 31978/tcp): CLEAN (Timeout)
|   Check 2 (port 56937/tcp): CLEAN (Timeout)
|   Check 3 (port 3506/udp): CLEAN (Timeout)
|   Check 4 (port 50429/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-time: 
|   date: 2024-06-19T23:10:55
|_  start_date: N/A
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required
|_clock-skew: mean: 0s, deviation: 0s, median: 0s

TRACEROUTE (using port 3389/tcp)
HOP RTT      ADDRESS
1   59.10 ms ATTACKER
2   59.04 ms ATTACKER
3   59.42 ms TARGET
4   59.44 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 19 19:11:32 2024 -- 1 IP address (1 host up) scanned in 545.63 seconds

```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Wed Jun 19 19:02:26 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-06-19 19:02:27 EDT for 204s
Not shown: 65515 filtered tcp ports (no-response)
PORT      STATE SERVICE       REASON          VERSION
53/tcp    open  domain        syn-ack ttl 125 Simple DNS Plus
88/tcp    open  kerberos-sec  syn-ack ttl 125 Microsoft Windows Kerberos (server time: 2024-06-19 23:04:11Z)
135/tcp   open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
389/tcp   open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: heist.offsec0., Site: Default-First-Site-Name)
445/tcp   open  microsoft-ds? syn-ack ttl 125
464/tcp   open  kpasswd5?     syn-ack ttl 125
593/tcp   open  ncacn_http    syn-ack ttl 125 Microsoft Windows RPC over HTTP 1.0
636/tcp   open  tcpwrapped    syn-ack ttl 125
3268/tcp  open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: heist.offsec0., Site: Default-First-Site-Name)
3269/tcp  open  tcpwrapped    syn-ack ttl 125
3389/tcp  open  ms-wbt-server syn-ack ttl 125 Microsoft Terminal Services
|_ssl-date: 2024-06-19T23:05:49+00:00; 0s from scanner time.
| rdp-ntlm-info: 
|   Target_Name: HEIST
|   NetBIOS_Domain_Name: HEIST
|   NetBIOS_Computer_Name: DC01
|   DNS_Domain_Name: heist.offsec
|   DNS_Computer_Name: DC01.heist.offsec
|   DNS_Tree_Name: heist.offsec
|   Product_Version: 10.0.17763
|_  System_Time: 2024-06-19T23:05:10+00:00
| ssl-cert: Subject: commonName=DC01.heist.offsec
| Issuer: commonName=DC01.heist.offsec
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-06-18T23:00:58
| Not valid after:  2024-12-18T23:00:58
| MD5:   6f7f:333b:d462:cbe8:0df1:1536:9bcf:fed5
| SHA-1: a327:0056:3b82:99af:9100:a348:985b:7f9b:88f8:ab22
| -----BEGIN CERTIFICATE-----
| MIIC5jCCAc6gAwIBAgIQXn4vqQ62UK5Dcpm6JoAr+TANBgkqhkiG9w0BAQsFADAc
| MRowGAYDVQQDExFEQzAxLmhlaXN0Lm9mZnNlYzAeFw0yNDA2MTgyMzAwNThaFw0y
| NDEyMTgyMzAwNThaMBwxGjAYBgNVBAMTEURDMDEuaGVpc3Qub2Zmc2VjMIIBIjAN
| BgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAs8sIVBQ+kyaS9rsGgLCEo/vTIGiu
| QXQu2CA2GBW0Ew87d+fwRWHC3Y2ELEqfQAbiaE2X2yKZlCDVPoS6eEuGfCqldZs0
| DqZU1XZifLH1xPEPihmY+gvf5PBWNYmMFUR/SS76HQuSypuDs5fCICVYjZJzgG8a
| no0oO5zHL5dOJZTM91adFFC+pkkf1p3cah8pk/PkkFZpEQkvc+osicDdSFs+oIPc
| JBFbeuvEqttjY5i6n2xBjal7A6uHsrod2dn4z21pQtZxsJfV1hit1/7QGRNq6XcS
| I5hCnCxXPCnEmjbSgJkVcccdWkW9brvNVyg56gocsXTWEY1L+fNXb1S58QIDAQAB
| oyQwIjATBgNVHSUEDDAKBggrBgEFBQcDATALBgNVHQ8EBAMCBDAwDQYJKoZIhvcN
| AQELBQADggEBAEqpSvlVWaQ0mdidfr5Lv+MoQVsFr0MohN1p1n4SGSURNskTgPXK
| agLHDdseoxxwAAjIk82Bv2HbVnEboZHLEqS1tGpgRKS16vg/0WhOR6YMhM2slB/g
| LfyV2GF6eLNHEYRboHF5g30v/BBGm+wQ7E8cCGFJB+ARXYcWjKkAfZauamQx0UIY
| N9cpHHm9bhxZfeqV7JvcfpkCyYnO+HTPdGIynqY6PRWvx4HNm4Y7erSFGVwYjJiV
| Cl6MP7HD1VUWho4jmslFYSKqbyXoWYssbQdZ0pJwYgG91/71tvqH4GVRITinT5n5
| a1qzzCmXqmPY+OdZTjbX1aoDHsWOgsbJcxY=
|_-----END CERTIFICATE-----
5985/tcp  open  http          syn-ack ttl 125 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
8080/tcp  open  http          syn-ack ttl 125 Werkzeug httpd 2.0.1 (Python 3.9.0)
|_http-server-header: Werkzeug/2.0.1 Python/3.9.0
| http-methods: 
|_  Supported Methods: OPTIONS GET HEAD
|_http-title: Super Secure Web Browser
9389/tcp  open  mc-nmf        syn-ack ttl 125 .NET Message Framing
49666/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49668/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49673/tcp open  ncacn_http    syn-ack ttl 125 Microsoft Windows RPC over HTTP 1.0
49674/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49677/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
No OS matches for host
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=6/19%OT=53%CT=%CU=%PV=Y%DS=4%DC=T%G=N%TM=6673644F%P=x86_64-pc-linux-gnu)
SEQ(SP=104%GCD=1%ISR=10C%TI=I%TS=U)
SEQ(SP=104%GCD=1%ISR=10D%TI=I%TS=U)
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
TCP Sequence Prediction: Difficulty=260 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: Host: DC01; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2024-06-19T23:05:14
|_  start_date: N/A
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 31978/tcp): CLEAN (Timeout)
|   Check 2 (port 56937/tcp): CLEAN (Timeout)
|   Check 3 (port 3506/udp): CLEAN (Timeout)
|   Check 4 (port 50429/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
|_clock-skew: mean: 0s, deviation: 0s, median: 0s

TRACEROUTE (using port 53/tcp)
HOP RTT      ADDRESS
1   58.81 ms ATTACKER
2   58.70 ms ATTACKER
3   58.85 ms TARGET
4   59.31 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 19 19:05:51 2024 -- 1 IP address (1 host up) scanned in 204.83 seconds


```

#### UDP scan
```


```

