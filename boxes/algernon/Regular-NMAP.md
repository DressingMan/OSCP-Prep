```
# Nmap 7.94SVN scan initiated Mon Jun 24 23:03:00 2024 as: nmap -p- -sV -sC --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up (0.073s latency).
Not shown: 64095 closed tcp ports (reset), 1426 filtered tcp ports (no-response)
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
# Nmap done at Mon Jun 24 23:06:22 2024 -- 1 IP address (1 host up) scanned in 201.94 seconds
```
