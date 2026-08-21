## Host Info
```
TARGET

OS details: Linux 2.6.18
```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Fri Jun 21 08:57:24 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.063s latency).
Scanned at 2024-06-21 08:57:24 EDT for 18s
Not shown: 998 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http Apache httpd 2.4.56 ((Debian))
|_http-title: PluXml - Blog or CMS, XML powered !
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Fri Jun 21 08:57:42 2024 -- 1 IP address (1 host up) scanned in 18.23 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Fri Jun 21 08:57:24 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-06-21 08:57:24 EDT for 76s
Not shown: 65533 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http Apache httpd 2.4.56 ((Debian))
| http-methods:
|_http-title: PluXml - Blog or CMS, XML powered !
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Fri Jun 21 08:58:40 2024 -- 1 IP address (1 host up) scanned in 76.15 seconds
```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Fri Jun 21 08:57:24 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.064s latency).
Scanned at 2024-06-21 08:57:24 EDT for 231s
Not shown: 78 closed udp ports (port-unreach)
PORT      STATE SERVICE        VERSION
# Nmap done at Fri Jun 21 09:01:15 2024 -- 1 IP address (1 host up) scanned in 231.38 seconds
# UDP: 22 open|filtered omitted (none confirmed open)
```

