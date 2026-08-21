```bash
# Nmap 7.94SVN scan initiated Wed Jul 24 18:00:23 2024 as: nmap -p- -sV -sC --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up (0.063s latency).
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
# Nmap done at Wed Jul 24 18:03:47 2024 -- 1 IP address (1 host up) scanned in 204.01 seconds
```
