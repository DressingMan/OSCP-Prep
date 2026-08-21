## Host Info
```
TARGET
```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Wed Jun 19 22:52:25 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.060s latency).
Scanned at 2024-06-19 22:52:25 EDT for 28s
Not shown: 998 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
80/tcp open http Apache httpd 2.4.41
| http-methods:
|_http-title: Index of /
Service Info: Host: 127.0.0.1; OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Wed Jun 19 22:52:53 2024 -- 1 IP address (1 host up) scanned in 27.86 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Wed Jun 19 22:52:25 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-06-19 22:52:25 EDT for 755s
Not shown: 65533 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
80/tcp open http Apache httpd 2.4.41
| http-methods:
|_http-title: Index of /
Service Info: Host: 127.0.0.1; OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Wed Jun 19 23:05:00 2024 -- 1 IP address (1 host up) scanned in 755.35 seconds
```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Wed Jun 19 22:52:25 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.065s latency).
Scanned at 2024-06-19 22:52:25 EDT for 204s
Not shown: 84 closed udp ports (port-unreach)
PORT      STATE SERVICE        VERSION
# Nmap done at Wed Jun 19 22:55:49 2024 -- 1 IP address (1 host up) scanned in 204.36 seconds
# UDP: 16 open|filtered omitted (none confirmed open)
```

