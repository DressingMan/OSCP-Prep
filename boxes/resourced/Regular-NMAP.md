```bash
# Nmap 7.94SVN scan initiated Wed Jul 24 19:14:59 2024 as: nmap -p- -sV -sC --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up (0.062s latency).
Not shown: 65515 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
53/tcp open domain?
88/tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2024-07-24 23:17:04Z)
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
389/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: resourced.local0., Site: Defau...
445/tcp open microsoft-ds?
464/tcp open kpasswd5?
593/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
636/tcp open tcpwrapped
3268/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: resourced.local0., Site: Defa...
3269/tcp open tcpwrapped
3389/tcp open ms-wbt-server Microsoft Terminal Services
| ssl-cert: Subject: commonName=ResourceDC.resourced.local
5985/tcp open http Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
9389/tcp open mc-nmf .NET Message Framing
49666/tcp open msrpc Microsoft Windows RPC
49668/tcp open msrpc Microsoft Windows RPC
49674/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
49675/tcp open msrpc Microsoft Windows RPC
49695/tcp open msrpc Microsoft Windows RPC
49711/tcp open msrpc Microsoft Windows RPC
Service Info: Host: RESOURCEDC; OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled and required
# Nmap done at Wed Jul 24 19:20:05 2024 -- 1 IP address (1 host up) scanned in 305.81 seconds
```
