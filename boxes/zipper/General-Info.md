## Host Info
```bash
TARGET

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Tue Jul 16 15:01:00 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.089s latency).
Scanned at 2024-07-16 15:01:01 EDT for 20s
Not shown: 998 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.2p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
80/tcp open http Apache httpd 2.4.41 ((Ubuntu))
| http-methods:
|_http-title: Zipper
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Tue Jul 16 15:01:21 2024 -- 1 IP address (1 host up) scanned in 20.70 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Tue Jul 16 15:01:00 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-07-16 15:01:01 EDT for 100s
Not shown: 65533 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.2p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
80/tcp open http Apache httpd 2.4.41 ((Ubuntu))
| http-methods:
|_http-title: Zipper
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Tue Jul 16 15:02:42 2024 -- 1 IP address (1 host up) scanned in 101.72 seconds
```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Tue Jul 16 15:01:00 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.067s latency).
Scanned at 2024-07-16 15:01:01 EDT for 210s
Not shown: 86 closed udp ports (port-unreach)
PORT      STATE SERVICE        VERSION
# Nmap done at Tue Jul 16 15:04:32 2024 -- 1 IP address (1 host up) scanned in 211.61 seconds
# UDP: 14 open|filtered omitted (none confirmed open)
```

