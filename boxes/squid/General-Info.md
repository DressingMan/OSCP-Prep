## Host Info
```bash
TARGET

64-bit

Windows 

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Wed Jul 24 17:59:58 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-07-24 17:59:58 EDT for 108s
Not shown: 996 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
445/tcp open microsoft-ds?
3128/tcp open http-proxy Squid http proxy 4.14
|_http-title: ERROR: The requested URL could not be retrieved
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Wed Jul 24 18:01:46 2024 -- 1 IP address (1 host up) scanned in 108.04 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Wed Jul 24 17:59:58 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-07-24 17:59:58 EDT for 199s
Not shown: 65529 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
445/tcp open microsoft-ds?
3128/tcp open http-proxy Squid http proxy 4.14
|_http-title: ERROR: The requested URL could not be retrieved
49666/tcp open msrpc Microsoft Windows RPC
49667/tcp open msrpc Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Wed Jul 24 18:03:17 2024 -- 1 IP address (1 host up) scanned in 199.02 seconds
```

#### UDP scan
```bash

```

