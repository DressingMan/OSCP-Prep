```bash
# Nmap 7.94SVN scan initiated Sat Jul 27 21:38:57 2024 as: nmap -p- -sV -sC --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up (0.060s latency).
Not shown: 65514 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
53/tcp open domain Simple DNS Plus
80/tcp open http Apache httpd 2.4.48 ((Win64) OpenSSL/1.1.1k PHP/8.0.7)
| http-methods:
|_  Potentially risky methods: TRACE
|_http-title: Access The Event
88/tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2024-07-28 01:40:51Z)
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
389/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: access.offsec0., Site: Default...
445/tcp open microsoft-ds?
464/tcp open kpasswd5?
593/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
636/tcp open tcpwrapped
3268/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: access.offsec0., Site: Defaul...
3269/tcp open tcpwrapped
5985/tcp open http Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
9389/tcp open mc-nmf .NET Message Framing
49666/tcp open msrpc Microsoft Windows RPC
49668/tcp open msrpc Microsoft Windows RPC
49673/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
49674/tcp open msrpc Microsoft Windows RPC
49677/tcp open msrpc Microsoft Windows RPC
49706/tcp open msrpc Microsoft Windows RPC
49799/tcp open msrpc Microsoft Windows RPC
Service Info: Host: SERVER; OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled and required
# Nmap done at Sat Jul 27 21:42:21 2024 -- 1 IP address (1 host up) scanned in 203.77 seconds
```
