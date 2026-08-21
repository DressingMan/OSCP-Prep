## NMAP 

```
# Nmap 7.94SVN scan initiated Mon Jun 24 23:13:44 2024 as: nmap -vv --reason -Pn -T4 -sV -p 49669 --script=banner,msrpc-enum,rpc-grind,rpcinfo TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-06-24 23:13:44 EDT for 70s
PORT      STATE SERVICE        VERSION
49669/tcp open msrpc Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
# Nmap done at Mon Jun 24 23:14:54 2024 -- 1 IP address (1 host up) scanned in 70.53 seconds
```

