## Host Info
```bash

TARGET

ASP.NET

64bit 

hutch.offsec

rootDomainNamingContext: DC=hutch,DC=offsec

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Mon Jul 15 15:21:47 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-07-15 15:21:47 EDT for 546s
Not shown: 988 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
53/tcp open domain?
80/tcp open http Microsoft IIS httpd 10.0
| http-methods:
|_  Potentially risky methods: TRACE COPY PROPFIND DELETE MOVE PROPPATCH MKCOL LOCK UNLOCK PUT
|_http-title: IIS Windows Server
88/tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2024-07-15 19:21:59Z)
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
389/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: hutch.offsec0., Site: Default-...
445/tcp open microsoft-ds?
464/tcp open kpasswd5?
593/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
636/tcp open tcpwrapped
3268/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: hutch.offsec0., Site: Default...
3269/tcp open tcpwrapped
Service Info: Host: HUTCHDC; OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled and required
# Nmap done at Mon Jul 15 15:30:53 2024 -- 1 IP address (1 host up) scanned in 546.21 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Mon Jul 15 15:21:47 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-07-15 15:21:47 EDT for 221s
Not shown: 65515 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
53/tcp open domain Simple DNS Plus
80/tcp open http Microsoft IIS httpd 10.0
| http-methods:
|_  Potentially risky methods: TRACE COPY PROPFIND DELETE MOVE PROPPATCH MKCOL LOCK UNLOCK PUT
|_http-title: IIS Windows Server
88/tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2024-07-15 19:23:45Z)
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
389/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: hutch.offsec0., Site: Default-...
445/tcp open microsoft-ds?
464/tcp open kpasswd5?
593/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
636/tcp open tcpwrapped
3268/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: hutch.offsec0., Site: Default...
3269/tcp open tcpwrapped
5985/tcp open http Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
9389/tcp open mc-nmf .NET Message Framing
49666/tcp open msrpc Microsoft Windows RPC
49668/tcp open msrpc Microsoft Windows RPC
49673/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
49674/tcp open msrpc Microsoft Windows RPC
49676/tcp open msrpc Microsoft Windows RPC
49692/tcp open msrpc Microsoft Windows RPC
Service Info: Host: HUTCHDC; OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled and required
# Nmap done at Mon Jul 15 15:25:28 2024 -- 1 IP address (1 host up) scanned in 221.93 seconds
```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Mon Jul 15 15:21:47 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.060s latency).
Scanned at 2024-07-15 15:21:48 EDT for 1776s
Not shown: 97 open|filtered udp ports (no-response)
PORT      STATE SERVICE        VERSION
53/udp open domain udp-response ttl 125 (generic dns response: NOTIMP)
88/udp open kerberos-sec udp-response ttl 125 Microsoft Windows Kerberos (server time: 2024-07-15...
123/udp open ntp udp-response ttl 125 NTP v3
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
# Nmap done at Mon Jul 15 15:51:24 2024 -- 1 IP address (1 host up) scanned in 1777.86 seconds
```

