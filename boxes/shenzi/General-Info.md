## Host Info
```
TARGET

```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:18:41 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.070s latency).
Scanned at 2024-06-26 21:18:41 EDT for 72s
Not shown: 993 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
21/tcp open ftp FileZilla ftpd 0.9.41 beta
80/tcp open http Apache httpd 2.4.43 ((Win64) OpenSSL/1.1.1g PHP/7.4.6)
| http-title: Welcome to XAMPP
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
443/tcp open ssl/http Apache httpd 2.4.43 ((Win64) OpenSSL/1.1.1g PHP/7.4.6)
| http-title: Welcome to XAMPP
| ssl-cert: Subject: commonName=localhost
445/tcp open microsoft-ds?
3306/tcp open mysql?
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Wed Jun 26 21:19:53 2024 -- 1 IP address (1 host up) scanned in 72.47 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:18:41 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.069s latency).
Scanned at 2024-06-26 21:18:41 EDT for 619s
Not shown: 65520 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
21/tcp open ftp FileZilla ftpd 0.9.41 beta
80/tcp open http Apache httpd 2.4.43 ((Win64) OpenSSL/1.1.1g PHP/7.4.6)
| http-title: Welcome to XAMPP
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
443/tcp open ssl/http Apache httpd 2.4.43 ((Win64) OpenSSL/1.1.1g PHP/7.4.6)
| ssl-cert: Subject: commonName=localhost
| http-title: Welcome to XAMPP
445/tcp open microsoft-ds?
3306/tcp open mysql?
5040/tcp open unknown
7680/tcp open pando-pub?
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
# Nmap done at Wed Jun 26 21:29:00 2024 -- 1 IP address (1 host up) scanned in 619.10 seconds
```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:18:41 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.071s latency).
Scanned at 2024-06-26 21:18:41 EDT for 412s
Not shown: 81 closed udp ports (port-unreach)
PORT      STATE SERVICE        VERSION
# Nmap done at Wed Jun 26 21:25:33 2024 -- 1 IP address (1 host up) scanned in 412.29 seconds
# UDP: 19 open|filtered omitted (none confirmed open)
```

