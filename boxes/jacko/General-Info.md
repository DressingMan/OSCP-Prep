## Host Info
```
TARGET

windows

```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Sat Jun 29 17:49:57 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.055s latency).
Scanned at 2024-06-29 17:49:57 EDT for 110s
Not shown: 995 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
80/tcp open http Microsoft IIS httpd 10.0
|_http-title: H2 Database Engine (redirect)
| http-methods:
|_  Potentially risky methods: TRACE
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
445/tcp open microsoft-ds?
8082/tcp open http H2 database http console
| http-methods:
|_http-title: H2 Console
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Sat Jun 29 17:51:47 2024 -- 1 IP address (1 host up) scanned in 109.61 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Sat Jun 29 17:49:57 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.074s latency).
Scanned at 2024-06-29 17:49:57 EDT for 231s
Not shown: 65529 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
80/tcp open http Microsoft IIS httpd 10.0
| http-methods:
|_  Potentially risky methods: TRACE
|_http-title: H2 Database Engine (redirect)
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
445/tcp open microsoft-ds?
7680/tcp open pando-pub?
8082/tcp open http H2 database http console
|_http-title: H2 Console
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Sat Jun 29 17:53:48 2024 -- 1 IP address (1 host up) scanned in 230.86 seconds
```

#### UDP scan
```

```

