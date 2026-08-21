## NMAP 

```
# Nmap 7.94SVN scan initiated Wed Jun 19 19:05:52 2024 as: nmap -vv --reason -Pn -T4 -sV -p 49666 --script=banner,msrpc-enum,rpc-grind,rpcinfo TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.075s latency).
Scanned at 2024-06-19 19:05:53 EDT for 71s
PORT      STATE SERVICE        VERSION
49666/tcp open msrpc Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
# Nmap done at Wed Jun 19 19:07:04 2024 -- 1 IP address (1 host up) scanned in 72.24 seconds
```
