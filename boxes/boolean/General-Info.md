## Host Info
```
TARGET

Linux 
```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Sat Jun 29 20:51:17 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.078s latency).
Scanned at 2024-06-29 20:51:17 EDT for 69s
Not shown: 997 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
80/tcp open http
| http-title: Boolean
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Sat Jun 29 20:52:26 2024 -- 1 IP address (1 host up) scanned in 68.80 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Sat Jun 29 20:51:17 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.053s latency).
Scanned at 2024-06-29 20:51:17 EDT for 311s
Not shown: 65531 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
80/tcp open http
| http-title: Boolean
33017/tcp open http Apache httpd 2.4.38 ((Debian))
| http-methods:
|_http-title: Development
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Sat Jun 29 20:56:28 2024 -- 1 IP address (1 host up) scanned in 310.78 seconds
```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Sat Jun 29 20:51:17 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.053s latency).
Scanned at 2024-06-29 20:51:18 EDT for 1822s
# Nmap done at Sat Jun 29 21:21:40 2024 -- 1 IP address (1 host up) scanned in 1822.87 seconds
```

