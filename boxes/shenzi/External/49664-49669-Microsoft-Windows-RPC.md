## NMAP 

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:29:00 2024 as: nmap -vv --reason -Pn -T4 -sV -p 49668 --script=banner,msrpc-enum,rpc-grind,rpcinfo -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.075s latency).
Scanned at 2024-06-26 21:29:01 EDT for 70s

PORT      STATE SERVICE REASON          VERSION
49668/tcp open  msrpc   syn-ack ttl 125 Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 26 21:30:11 2024 -- 1 IP address (1 host up) scanned in 70.85 seconds

```

