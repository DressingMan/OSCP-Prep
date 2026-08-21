## Host Info
```
TARGET

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Thu Oct 24 16:31:20 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-10-24 16:31:20 EDT for 18s
Not shown: 998 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http Apache httpd 2.4.56 ((Debian))
| http-methods:
|_http-title: htmLawed (1.2.5) test
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Thu Oct 24 16:31:38 2024 -- 1 IP address (1 host up) scanned in 18.92 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Thu Oct 24 16:31:20 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.055s latency).
Scanned at 2024-10-24 16:31:20 EDT for 76s
Not shown: 65533 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http Apache httpd 2.4.56 ((Debian))
| http-methods:
|_http-title: htmLawed (1.2.5) test
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Thu Oct 24 16:32:36 2024 -- 1 IP address (1 host up) scanned in 76.85 seconds
```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Thu Oct 24 16:33:34 2024 as: nmap -vvv --top-ports 100 -sU -oN nmap_udp TARGET
Nmap scan report for TARGET
Host is up, received reset ttl 61 (0.054s latency).
Scanned at 2024-10-24 16:33:34 EDT for 137s
PORT      STATE SERVICE        VERSION
```

#### Regular NMAP
```bash
# Nmap 7.94SVN scan initiated Thu Oct 24 16:31:23 2024 as: nmap -p- -sV -sC -vvv --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.061s latency).
Scanned at 2024-10-24 16:31:23 EDT for 35s
Not shown: 65371 closed tcp ports (reset), 162 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http Apache httpd 2.4.56 ((Debian))
| http-methods:
|_http-title: htmLawed (1.2.5) test
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Thu Oct 24 16:31:58 2024 -- 1 IP address (1 host up) scanned in 34.78 seconds
```

