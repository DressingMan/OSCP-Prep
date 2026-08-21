## Host Info
```bash
TARGET

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Thu Jul 11 17:18:43 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.052s latency).
Scanned at 2024-07-11 17:18:44 EDT for 121s
Not shown: 998 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
80/tcp open http Apache httpd 2.4.41 ((Ubuntu))
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Thu Jul 11 17:20:45 2024 -- 1 IP address (1 host up) scanned in 122.24 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Thu Jul 11 17:18:43 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.051s latency).
Scanned at 2024-07-11 17:18:44 EDT for 227s
Not shown: 65533 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
80/tcp open http Apache httpd 2.4.41 ((Ubuntu))
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Thu Jul 11 17:22:31 2024 -- 1 IP address (1 host up) scanned in 227.73 seconds
```

#### UDP scan
```bash

```

