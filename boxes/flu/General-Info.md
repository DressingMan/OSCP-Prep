## Host Info
```

TARGET

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Wed Oct 30 15:17:44 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.056s latency).
Scanned at 2024-10-30 15:17:44 EDT for 28s
Not shown: 998 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 9.0p1 Ubuntu 1ubuntu8.5 (Ubuntu Linux; protocol 2.0)
8090/tcp open opsmessaging?
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Wed Oct 30 15:18:12 2024 -- 1 IP address (1 host up) scanned in 28.30 seconds
```

#### Full Scan
```bash

```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Wed Oct 30 15:18:16 2024 as: nmap -vvv --top-ports 100 -sU -oN nmap_udp TARGET
Nmap scan report for TARGET
Host is up, received reset ttl 61 (0.056s latency).
Scanned at 2024-10-30 15:18:16 EDT for 139s
PORT      STATE SERVICE        VERSION
```

#### Regular NMAP
```bash
# Nmap 7.94SVN scan initiated Wed Oct 30 15:18:09 2024 as: nmap -p- -sV -sC -vvv --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.059s latency).
Scanned at 2024-10-30 15:18:09 EDT for 133s
Not shown: 65405 closed tcp ports (reset), 127 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 9.0p1 Ubuntu 1ubuntu8.5 (Ubuntu Linux; protocol 2.0)
8090/tcp open opsmessaging?
8091/tcp open jamlink?
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Wed Oct 30 15:20:22 2024 -- 1 IP address (1 host up) scanned in 133.28 seconds
```

