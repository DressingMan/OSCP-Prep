## Host Info
```

 TARGET

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Mon Oct 21 15:59:14 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-10-21 15:59:15 EDT for 24s
Not shown: 997 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http Apache httpd 2.4.56 ((Debian))
|_http-title: Lugx Gaming Shop HTML5 Template
8089/tcp open http Apache httpd 2.4.56 ((Debian))
| http-methods:
|_http-title: FlatPress
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Oct 21 15:59:39 2024 -- 1 IP address (1 host up) scanned in 25.05 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Mon Oct 21 15:59:14 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.057s latency).
Scanned at 2024-10-21 15:59:15 EDT for 70s
Not shown: 65532 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http Apache httpd 2.4.56 ((Debian))
|_http-title: Lugx Gaming Shop HTML5 Template
8089/tcp open http Apache httpd 2.4.56 ((Debian))
|_http-title: FlatPress
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Oct 21 16:00:25 2024 -- 1 IP address (1 host up) scanned in 71.07 seconds
```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Mon Oct 21 15:59:14 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.057s latency).
Scanned at 2024-10-21 15:59:15 EDT for 307s
PORT      STATE SERVICE        VERSION
# UDP: 37 open|filtered omitted (none confirmed open)
```

#### Regular NMAP
```bash
# Nmap 7.94SVN scan initiated Mon Oct 21 16:06:25 2024 as: nmap -p- -sV -sC -vvv --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.057s latency).
Scanned at 2024-10-21 16:06:25 EDT for 40s
Not shown: 64704 closed tcp ports (reset), 828 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http Apache httpd 2.4.56 ((Debian))
|_http-title: Lugx Gaming Shop HTML5 Template
8089/tcp open http Apache httpd 2.4.56 ((Debian))
|_http-title: FlatPress
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Oct 21 16:07:05 2024 -- 1 IP address (1 host up) scanned in 40.24 seconds
```

