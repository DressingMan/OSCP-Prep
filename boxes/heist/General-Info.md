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
# Nmap 7.94SVN scan initiated Wed Jun 19 19:02:26 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.060s latency).
Scanned at 2024-06-19 19:02:27 EDT for 545s
Not shown: 987 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
53/tcp open domain?
88/tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2024-06-19 23:02:38Z)
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
389/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: heist.offsec0., Site: Default-...
445/tcp open microsoft-ds?
464/tcp open kpasswd5?
593/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
636/tcp open tcpwrapped
3268/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: heist.offsec0., Site: Default...
3269/tcp open tcpwrapped
3389/tcp open ms-wbt-server Microsoft Terminal Services
| ssl-cert: Subject: commonName=DC01.heist.offsec
8080/tcp open http Werkzeug httpd 2.0.1 (Python 3.9.0)
| http-methods:
|_http-title: Super Secure Web Browser
Service Info: Host: DC01; OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled and required
# Nmap done at Wed Jun 19 19:11:32 2024 -- 1 IP address (1 host up) scanned in 545.63 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Wed Jun 19 19:02:26 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-06-19 19:02:27 EDT for 204s
Not shown: 65515 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
53/tcp open domain Simple DNS Plus
88/tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2024-06-19 23:04:11Z)
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
389/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: heist.offsec0., Site: Default-...
445/tcp open microsoft-ds?
464/tcp open kpasswd5?
593/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
636/tcp open tcpwrapped
3268/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: heist.offsec0., Site: Default...
3269/tcp open tcpwrapped
3389/tcp open ms-wbt-server Microsoft Terminal Services
| ssl-cert: Subject: commonName=DC01.heist.offsec
5985/tcp open http Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
8080/tcp open http Werkzeug httpd 2.0.1 (Python 3.9.0)
| http-methods:
|_http-title: Super Secure Web Browser
9389/tcp open mc-nmf .NET Message Framing
49666/tcp open msrpc Microsoft Windows RPC
49668/tcp open msrpc Microsoft Windows RPC
49673/tcp open ncacn_http Microsoft Windows RPC over HTTP 1.0
49674/tcp open msrpc Microsoft Windows RPC
49677/tcp open msrpc Microsoft Windows RPC
Service Info: Host: DC01; OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled and required
# Nmap done at Wed Jun 19 19:05:51 2024 -- 1 IP address (1 host up) scanned in 204.83 seconds
```

#### UDP scan
```

```

