## Host Info
```
TARGET
```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Mon Jun 10 16:57:23 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.063s latency).
Scanned at 2024-06-10 16:57:24 EDT for 24s
Not shown: 999 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.3p1 Ubuntu 1ubuntu0.1 (Ubuntu Linux; protocol 2.0)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Jun 10 16:57:48 2024 -- 1 IP address (1 host up) scanned in 24.24 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Mon Jun 10 16:57:24 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.070s latency).
Scanned at 2024-06-10 16:57:24 EDT for 133s
Not shown: 65533 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.3p1 Ubuntu 1ubuntu0.1 (Ubuntu Linux; protocol 2.0)
6379/tcp open redis Redis key-value store 4.0.14
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Jun 10 16:59:37 2024 -- 1 IP address (1 host up) scanned in 133.50 seconds
```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Mon Jun 10 16:57:23 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.075s latency).
Scanned at 2024-06-10 16:57:24 EDT for 222s
Not shown: 82 closed udp ports (port-unreach)
PORT      STATE SERVICE        VERSION
# Nmap done at Mon Jun 10 17:01:06 2024 -- 1 IP address (1 host up) scanned in 222.66 seconds
# UDP: 18 open|filtered omitted (none confirmed open)
```

