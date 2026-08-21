## Host Info
```
TARGET

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Wed Oct  9 20:56:18 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.057s latency).
Scanned at 2024-10-09 20:56:18 EDT for 23s
Not shown: 997 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
21/tcp open ftp vsftpd 3.0.3
80/tcp open http Apache httpd 2.4.41
|_http-title: 403 Forbidden
Service Info: Host: 127.0.0.1; OS: Unix
# Nmap done at Wed Oct  9 20:56:41 2024 -- 1 IP address (1 host up) scanned in 22.79 seconds
```

#### Full Scan
```bash
Nmap scan report for TARGET
Host is up, received user-set (0.057s latency).
Scanned at 2024-10-09 20:56:18 EDT for 108s
Not shown: 65532 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
21/tcp open ftp vsftpd 3.0.3
80/tcp open http Apache httpd 2.4.41
| http-methods:
|_http-title: 403 Forbidden
Service Info: Host: 127.0.0.1; OS: Unix
# Nmap done at Wed Oct  9 20:58:06 2024 -- 1 IP address (1 host up) scanned in 107.60 seconds
```

#### UDP scan
```bash

```

