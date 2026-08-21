## Host Info
```bash
TARGET

Identified HTTP Server: Cheroot/8.6.0

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Mon Jul 15 22:05:45 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.069s latency).
Scanned at 2024-07-15 22:05:46 EDT for 48s
Not shown: 998 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.9p1 Ubuntu 3ubuntu0.1 (Ubuntu Linux; protocol 2.0)
9666/tcp open http CherryPy wsgiserver
| http-title: Login - pyLoad
| http-robots.txt: 1 disallowed entry
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Jul 15 22:06:34 2024 -- 1 IP address (1 host up) scanned in 49.11 seconds
```

#### Full Scan
```bash

```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Mon Jul 15 22:05:45 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.14s latency).
Scanned at 2024-07-15 22:05:46 EDT for 200s
Not shown: 91 closed udp ports (port-unreach)
PORT      STATE SERVICE        VERSION
# Nmap done at Mon Jul 15 22:09:06 2024 -- 1 IP address (1 host up) scanned in 201.31 seconds
# UDP: 9 open|filtered omitted (none confirmed open)
```

