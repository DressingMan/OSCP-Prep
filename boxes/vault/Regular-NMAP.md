```bash
# Nmap 7.94SVN scan initiated Sat Jul 27 19:16:35 2024 as: nmap -p- -sV -sC --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up (0.058s latency).
Not shown: 65514 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
53/tcp open domain?
88/tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2024-07-27 23:18:27Z)
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
389/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: vault.offsec0., Site: Default-...
445/tcp open microsoft-ds?
464/tcp open kpasswd5?
593/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
636/tcp open tcpwrapped
3268/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: vault.offsec0., Site: Default...
3269/tcp open tcpwrapped
3389/tcp open ms-wbt-server Microsoft Terminal Services
| ssl-cert: Subject: commonName=DC.vault.offsec
5985/tcp open http Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
9389/tcp open mc-nmf .NET Message Framing
49666/tcp open msrpc Microsoft Windows RPC
49667/tcp open msrpc Microsoft Windows RPC
49673/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
49674/tcp open msrpc Microsoft Windows RPC
49679/tcp open msrpc Microsoft Windows RPC
49706/tcp open msrpc Microsoft Windows RPC
49826/tcp open msrpc Microsoft Windows RPC
Service Info: Host: DC; OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled and required
# Nmap done at Sat Jul 27 19:21:27 2024 -- 1 IP address (1 host up) scanned in 292.13 seconds
```

