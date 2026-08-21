## Host Info
```bash
TARGET
 
64-bit

```


## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Wed Jul 24 19:14:31 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.060s latency).
Scanned at 2024-07-24 19:14:32 EDT for 550s
Not shown: 988 filtered tcp ports (no-response)
PORT     STATE SERVICE       REASON          VERSION
53/tcp   open  domain?       syn-ack ttl 125
88/tcp   open  kerberos-sec  syn-ack ttl 125 Microsoft Windows Kerberos (server time: 2024-07-24 23:14:46Z)
135/tcp  open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
389/tcp  open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: resourced.local0., Site: Default-First-Site-Name)
445/tcp  open  microsoft-ds? syn-ack ttl 125
464/tcp  open  kpasswd5?     syn-ack ttl 125
593/tcp  open  ncacn_http    syn-ack ttl 125 Microsoft Windows RPC over HTTP 1.0
636/tcp  open  tcpwrapped    syn-ack ttl 125
3268/tcp open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: resourced.local0., Site: Default-First-Site-Name)
3269/tcp open  tcpwrapped    syn-ack ttl 125
3389/tcp open  ms-wbt-server syn-ack ttl 125 Microsoft Terminal Services
| rdp-ntlm-info: 
|   Target_Name: resourced
|   NetBIOS_Domain_Name: resourced
|   NetBIOS_Computer_Name: RESOURCEDC
|   DNS_Domain_Name: resourced.local
|   DNS_Computer_Name: ResourceDC.resourced.local
|   DNS_Tree_Name: resourced.local
|   Product_Version: 10.0.17763
|_  System_Time: 2024-07-24T23:22:59+00:00
| ssl-cert: Subject: commonName=ResourceDC.resourced.local
| Issuer: commonName=ResourceDC.resourced.local
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-07-23T23:12:55
| Not valid after:  2025-01-22T23:12:55
| MD5:   2716:01bb:cc23:4379:6ac8:543a:f11e:0e3d
| SHA-1: 34d8:6027:9d12:aabf:b2d2:1cb4:cc7f:cbdc:a12b:6322
| -----BEGIN CERTIFICATE-----
| MIIC+DCCAeCgAwIBAgIQIDPqZovwQ5JJ7zNNgBBAKTANBgkqhkiG9w0BAQsFADAl
| MSMwIQYDVQQDExpSZXNvdXJjZURDLnJlc291cmNlZC5sb2NhbDAeFw0yNDA3MjMy
| MzEyNTVaFw0yNTAxMjIyMzEyNTVaMCUxIzAhBgNVBAMTGlJlc291cmNlREMucmVz
| b3VyY2VkLmxvY2FsMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA0RTp
| sWixmARUjHHUBdt4cwFYZiq9sJfZqC05559jt+97oZXKjjXDmiHbaY/IaCwE1kJb
| T/UiOdoWXiuwXFXSa3/WOuF0V71JccGEHOZ8H3z2VGXaXjec+xJOAyVnJLX4RQ9C
| oFZ8DiBuPRBVdIArGdAFTiV7hwZ749wr4EK5teisHlKyFKESOlcYZEzdVgjTn2pk
| yA9RjWq89aFqyEdTaX6S5L5RrDjSS7wHADV3nYErfu+Oy4yrrGKY8htob46AUhoy
| Bu8tKwJDV2j+D6Ablyj6bt/qrUMLWoYrp0OEwUItGV+2zbAhzRn+dQuCWYnCyl0z
| 5TC2hDUwasnhQPi7QQIDAQABoyQwIjATBgNVHSUEDDAKBggrBgEFBQcDATALBgNV
| HQ8EBAMCBDAwDQYJKoZIhvcNAQELBQADggEBACalrQ7IA0pkydPedj1AZA+luYhW
| YaDVc4DNl5wIux4tU6Gc1zvwIVUCzJ6haA360RXk5XYRS2W1Qs/ax/VyaZmRt6k0
| dJTs2jyCwIk6fEsdHpMODUcukdbYx3MdT/xSZw3WKQrkueL0AyazknMrikxvwiZx
| go+tTo+yJ8qY2r0oW1nStooztNkmDSSxmlwRez6tny4gATznKSsW1HcZriOd+7vV
| 63FND/Ak6YjR54xTyE5hGeGyPpaXKYg7lLhVh6tFBgZky2l7jO4gPgq+ZHD3ea01
| pTV6vw7ErsBgOhU6HeyzpYg9zJrqUH479MLLSdTePVrKTWZBWAgWX9HcWdc=
|_-----END CERTIFICATE-----
|_ssl-date: 2024-07-24T23:23:39+00:00; -1s from scanner time.
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
No OS matches for host
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=7/24%OT=53%CT=%CU=%PV=Y%DS=4%DC=T%G=N%TM=66A18CFE%P=x86_64-pc-linux-gnu)
SEQ(SP=107%GCD=1%ISR=10C%TI=I%TS=U)
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
TCP Sequence Prediction: Difficulty=263 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: Host: RESOURCEDC; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 20408/tcp): CLEAN (Timeout)
|   Check 2 (port 59127/tcp): CLEAN (Timeout)
|   Check 3 (port 9933/udp): CLEAN (Timeout)
|   Check 4 (port 57262/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required
|_clock-skew: mean: -1s, deviation: 0s, median: -1s
| smb2-time: 
|   date: 2024-07-24T23:23:00
|_  start_date: N/A

TRACEROUTE (using port 445/tcp)
HOP RTT      ADDRESS
1   57.72 ms ATTACKER
2   57.71 ms ATTACKER
3   58.93 ms TARGET
4   59.97 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jul 24 19:23:42 2024 -- 1 IP address (1 host up) scanned in 551.18 seconds

```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Wed Jul 24 19:14:31 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.056s latency).
Scanned at 2024-07-24 19:14:32 EDT for 217s
Not shown: 65515 filtered tcp ports (no-response)
PORT      STATE SERVICE       REASON          VERSION
53/tcp    open  domain        syn-ack ttl 125 Simple DNS Plus
88/tcp    open  kerberos-sec  syn-ack ttl 125 Microsoft Windows Kerberos (server time: 2024-07-24 23:16:25Z)
135/tcp   open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
389/tcp   open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: resourced.local0., Site: Default-First-Site-Name)
445/tcp   open  microsoft-ds? syn-ack ttl 125
464/tcp   open  kpasswd5?     syn-ack ttl 125
593/tcp   open  ncacn_http    syn-ack ttl 125 Microsoft Windows RPC over HTTP 1.0
636/tcp   open  tcpwrapped    syn-ack ttl 125
3268/tcp  open  ldap          syn-ack ttl 125 Microsoft Windows Active Directory LDAP (Domain: resourced.local0., Site: Default-First-Site-Name)
3269/tcp  open  tcpwrapped    syn-ack ttl 125
3389/tcp  open  ms-wbt-server syn-ack ttl 125 Microsoft Terminal Services
| ssl-cert: Subject: commonName=ResourceDC.resourced.local
| Issuer: commonName=ResourceDC.resourced.local
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-07-23T23:12:55
| Not valid after:  2025-01-22T23:12:55
| MD5:   2716:01bb:cc23:4379:6ac8:543a:f11e:0e3d
| SHA-1: 34d8:6027:9d12:aabf:b2d2:1cb4:cc7f:cbdc:a12b:6322
| -----BEGIN CERTIFICATE-----
| MIIC+DCCAeCgAwIBAgIQIDPqZovwQ5JJ7zNNgBBAKTANBgkqhkiG9w0BAQsFADAl
| MSMwIQYDVQQDExpSZXNvdXJjZURDLnJlc291cmNlZC5sb2NhbDAeFw0yNDA3MjMy
| MzEyNTVaFw0yNTAxMjIyMzEyNTVaMCUxIzAhBgNVBAMTGlJlc291cmNlREMucmVz
| b3VyY2VkLmxvY2FsMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA0RTp
| sWixmARUjHHUBdt4cwFYZiq9sJfZqC05559jt+97oZXKjjXDmiHbaY/IaCwE1kJb
| T/UiOdoWXiuwXFXSa3/WOuF0V71JccGEHOZ8H3z2VGXaXjec+xJOAyVnJLX4RQ9C
| oFZ8DiBuPRBVdIArGdAFTiV7hwZ749wr4EK5teisHlKyFKESOlcYZEzdVgjTn2pk
| yA9RjWq89aFqyEdTaX6S5L5RrDjSS7wHADV3nYErfu+Oy4yrrGKY8htob46AUhoy
| Bu8tKwJDV2j+D6Ablyj6bt/qrUMLWoYrp0OEwUItGV+2zbAhzRn+dQuCWYnCyl0z
| 5TC2hDUwasnhQPi7QQIDAQABoyQwIjATBgNVHSUEDDAKBggrBgEFBQcDATALBgNV
| HQ8EBAMCBDAwDQYJKoZIhvcNAQELBQADggEBACalrQ7IA0pkydPedj1AZA+luYhW
| YaDVc4DNl5wIux4tU6Gc1zvwIVUCzJ6haA360RXk5XYRS2W1Qs/ax/VyaZmRt6k0
| dJTs2jyCwIk6fEsdHpMODUcukdbYx3MdT/xSZw3WKQrkueL0AyazknMrikxvwiZx
| go+tTo+yJ8qY2r0oW1nStooztNkmDSSxmlwRez6tny4gATznKSsW1HcZriOd+7vV
| 63FND/Ak6YjR54xTyE5hGeGyPpaXKYg7lLhVh6tFBgZky2l7jO4gPgq+ZHD3ea01
| pTV6vw7ErsBgOhU6HeyzpYg9zJrqUH479MLLSdTePVrKTWZBWAgWX9HcWdc=
|_-----END CERTIFICATE-----
| rdp-ntlm-info: 
|   Target_Name: resourced
|   NetBIOS_Domain_Name: resourced
|   NetBIOS_Computer_Name: RESOURCEDC
|   DNS_Domain_Name: resourced.local
|   DNS_Computer_Name: ResourceDC.resourced.local
|   DNS_Tree_Name: resourced.local
|   Product_Version: 10.0.17763
|_  System_Time: 2024-07-24T23:17:26+00:00
|_ssl-date: 2024-07-24T23:18:06+00:00; -1s from scanner time.
5985/tcp  open  http          syn-ack ttl 125 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
9389/tcp  open  mc-nmf        syn-ack ttl 125 .NET Message Framing
49666/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49668/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49674/tcp open  ncacn_http    syn-ack ttl 125 Microsoft Windows RPC over HTTP 1.0
49675/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49695/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49711/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
No OS matches for host
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=7/24%OT=53%CT=%CU=%PV=Y%DS=4%DC=T%G=N%TM=66A18BB1%P=x86_64-pc-linux-gnu)
SEQ(SP=107%GCD=1%ISR=10C%TI=I%TS=U)
SEQ(SP=107%GCD=2%ISR=10C%TI=I%TS=U)
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
TCP Sequence Prediction: Difficulty=263 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: Host: RESOURCEDC; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 20408/tcp): CLEAN (Timeout)
|   Check 2 (port 59127/tcp): CLEAN (Timeout)
|   Check 3 (port 9933/udp): CLEAN (Timeout)
|   Check 4 (port 57262/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-time: 
|   date: 2024-07-24T23:17:30
|_  start_date: N/A
|_clock-skew: mean: -1s, deviation: 0s, median: -2s
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required

TRACEROUTE (using port 53/tcp)
HOP RTT      ADDRESS
1   53.66 ms ATTACKER
2   53.64 ms ATTACKER
3   55.50 ms TARGET
4   55.81 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jul 24 19:18:09 2024 -- 1 IP address (1 host up) scanned in 217.95 seconds


```

#### UDP scan
```bash


```

