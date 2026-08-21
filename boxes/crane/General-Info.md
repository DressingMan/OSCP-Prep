## Host Info
```

TARGET

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:32:31 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-10-14 10:32:32 EDT for 19s
Not shown: 997 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
80/tcp open http Apache httpd 2.4.38 ((Debian))
| http-robots.txt: 1 disallowed entry
| http-title: SuiteCRM
3306/tcp open mysql MySQL (unauthorized)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Oct 14 10:32:51 2024 -- 1 IP address (1 host up) scanned in 19.93 seconds
```

#### Full Scan
```bash

```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:35:15 2024 as: nmap -vvv --top-ports 100 -sU -oN nmap_udp TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.056s latency).
Scanned at 2024-10-14 10:35:15 EDT for 2s
PORT      STATE SERVICE        VERSION
# UDP: 37 open|filtered omitted (none confirmed open)
```

#### Regular NMAP
```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:34:09 2024 as: nmap -p- -sV -sC -vvv --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.065s latency).
Scanned at 2024-10-14 10:34:09 EDT for 40s
Not shown: 65486 closed tcp ports (reset), 45 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
80/tcp open http Apache httpd 2.4.38 ((Debian))
| http-robots.txt: 1 disallowed entry
| http-title: SuiteCRM
3306/tcp open mysql MySQL (unauthorized)
33060/tcp open mysqlx?
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Oct 14 10:34:49 2024 -- 1 IP address (1 host up) scanned in 39.81 seconds
```

