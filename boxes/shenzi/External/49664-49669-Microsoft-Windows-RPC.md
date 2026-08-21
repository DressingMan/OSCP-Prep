## NMAP 

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:29:00 2024 as: nmap -vv --reason -Pn -T4 -sV -p 49668 --script=banner,msrpc-enum,rpc-grind,rpcinfo TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.075s latency).
Scanned at 2024-06-26 21:29:01 EDT for 70s
PORT      STATE SERVICE        VERSION
49668/tcp open msrpc Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
# Nmap done at Wed Jun 26 21:30:11 2024 -- 1 IP address (1 host up) scanned in 70.85 seconds
```

