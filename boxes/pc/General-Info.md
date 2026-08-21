## Host Info
```

TARGET

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Thu Oct 31 15:47:31 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.054s latency).
Scanned at 2024-10-31 15:47:32 EDT for 56s
Not shown: 998 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.2p1 Ubuntu 4ubuntu0.9 (Ubuntu Linux; protocol 2.0)
8000/tcp open http-alt ttyd/1.7.3-a2312cb (libwebsockets/3.2.0)
| http-methods:
|_http-title: ttyd - Terminal
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Thu Oct 31 15:48:28 2024 -- 1 IP address (1 host up) scanned in 57.31 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Thu Oct 31 15:47:31 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-10-31 15:47:32 EDT for 88s
Not shown: 65533 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.2p1 Ubuntu 4ubuntu0.9 (Ubuntu Linux; protocol 2.0)
8000/tcp open http-alt ttyd/1.7.3-a2312cb (libwebsockets/3.2.0)
|_http-title: ttyd - Terminal
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Thu Oct 31 15:49:00 2024 -- 1 IP address (1 host up) scanned in 88.88 seconds
```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Thu Oct 31 15:48:51 2024 as: nmap -vvv --top-ports 100 -sU -oN nmap_udp TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.055s latency).
Scanned at 2024-10-31 15:48:51 EDT for 136s
PORT      STATE SERVICE        VERSION
```
