## Host Info
```
TARGET

OS: Windows

ASP.NET

```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Mon Jun 24 23:02:58 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-06-24 23:02:58 EDT for 82s
Not shown: 994 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
21/tcp open ftp Microsoft ftpd
80/tcp open http Microsoft IIS httpd 10.0
| http-methods:
|_  Potentially risky methods: TRACE
|_http-title: IIS Windows
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
445/tcp open microsoft-ds?
9998/tcp open http Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
| http-title: Site doesn't have a title (text/html; charset=utf-8).
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Mon Jun 24 23:04:20 2024 -- 1 IP address (1 host up) scanned in 82.90 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Mon Jun 24 23:02:58 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-06-24 23:02:58 EDT for 645s
Not shown: 65521 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
21/tcp open ftp Microsoft ftpd
80/tcp open http Microsoft IIS httpd 10.0
|_http-title: IIS Windows
| http-methods:
|_  Potentially risky methods: TRACE
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
445/tcp open microsoft-ds?
5040/tcp open unknown
9998/tcp open http Microsoft IIS httpd 10.0
| http-title: Site doesn't have a title (text/html; charset=utf-8).
17001/tcp open remoting MS .NET Remoting services
49664/tcp open msrpc Microsoft Windows RPC
49665/tcp open msrpc Microsoft Windows RPC
49666/tcp open msrpc Microsoft Windows RPC
49667/tcp open msrpc Microsoft Windows RPC
49668/tcp open msrpc Microsoft Windows RPC
49669/tcp open msrpc Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Mon Jun 24 23:13:43 2024 -- 1 IP address (1 host up) scanned in 645.77 seconds
```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Mon Jun 24 23:02:58 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.060s latency).
Scanned at 2024-06-24 23:02:58 EDT for 392s
Not shown: 83 closed udp ports (port-unreach)
PORT      STATE SERVICE        VERSION
# Nmap done at Mon Jun 24 23:09:30 2024 -- 1 IP address (1 host up) scanned in 392.14 seconds
# UDP: 17 open|filtered omitted (none confirmed open)
```

