## NMAP 

```
# Nmap 7.94SVN scan initiated Sat Jul 27 21:38:38 2024 as: nmap -vv --reason -Pn -T4 -sV -p 49666 --script=banner,msrpc-enum,rpc-grind,rpcinfo TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.056s latency).
Scanned at 2024-07-27 21:38:39 EDT for 69s
PORT      STATE SERVICE        VERSION
49666/tcp open msrpc Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
# Nmap done at Sat Jul 27 21:39:48 2024 -- 1 IP address (1 host up) scanned in 70.29 seconds
```
