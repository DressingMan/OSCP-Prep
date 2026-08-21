## Host Info
```
TARGET

Linux 

```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Sat Jun 29 16:33:50 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.067s latency).
Scanned at 2024-06-29 16:33:50 EDT for 32s
Not shown: 996 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.4 (protocol 2.0)
53/tcp open domain NLnet Labs NSD
80/tcp open http nginx 1.16.1
|_http-title: Home | Mezzanine
8000/tcp open http nginx 1.16.1
| http-methods:
|_http-title: Site doesn't have a title (application/json).
# Nmap done at Sat Jun 29 16:34:22 2024 -- 1 IP address (1 host up) scanned in 32.68 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Sat Jun 29 16:33:49 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.068s latency).
Scanned at 2024-06-29 16:33:50 EDT for 144s
Not shown: 65529 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.4 (protocol 2.0)
53/tcp open domain NLnet Labs NSD
80/tcp open http nginx 1.16.1
|_http-title: Home | Mezzanine
4505/tcp open zmtp ZeroMQ ZMTP 2.0
4506/tcp open zmtp ZeroMQ ZMTP 2.0
8000/tcp open http nginx 1.16.1
| http-methods:
|_http-title: Site doesn't have a title (application/json).
# Nmap done at Sat Jun 29 16:36:14 2024 -- 1 IP address (1 host up) scanned in 145.00 seconds
```

#### UDP scan
```

```

