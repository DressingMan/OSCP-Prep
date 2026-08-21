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
# Nmap 7.94SVN scan initiated Sat Jul 27 19:16:11 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.056s latency).
Scanned at 2024-07-27 19:16:11 EDT for 543s
Not shown: 988 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
53/tcp open domain?
88/tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2024-07-27 23:16:22Z)
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
Service Info: Host: DC; OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled and required
# Nmap done at Sat Jul 27 19:25:14 2024 -- 1 IP address (1 host up) scanned in 543.51 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Sat Jul 27 19:16:11 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.056s latency).
Scanned at 2024-07-27 19:16:11 EDT for 208s
Not shown: 65514 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
53/tcp open domain Simple DNS Plus
88/tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2024-07-27 23:17:56Z)
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
# Nmap done at Sat Jul 27 19:19:39 2024 -- 1 IP address (1 host up) scanned in 208.04 seconds
```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Sat Jul 27 19:16:11 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-07-27 19:16:12 EDT for 1776s
Not shown: 97 open|filtered udp ports (no-response)
PORT      STATE SERVICE        VERSION
53/udp open domain udp-response ttl 125 (generic dns response: NOTIMP)
88/udp open kerberos-sec udp-response ttl 125 Microsoft Windows Kerberos (server time: 2024-07-27...
123/udp open ntp udp-response ttl 125 NTP v3
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
# Nmap done at Sat Jul 27 19:45:48 2024 -- 1 IP address (1 host up) scanned in 1777.69 seconds
```

