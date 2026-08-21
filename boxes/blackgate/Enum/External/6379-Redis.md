
```
# Nmap 7.94SVN scan initiated Mon Jun 10 16:59:37 2024 as: nmap -vv --reason -Pn -T4 -sV -p 6379 --script=banner,redis-info TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-06-10 16:59:37 EDT for 22s
PORT      STATE SERVICE        VERSION
6379/tcp open redis Redis key-value store 4.0.14 (64 bits)
# Nmap done at Mon Jun 10 16:59:59 2024 -- 1 IP address (1 host up) scanned in 21.51 seconds
```

```
redis_version: 4.0.14

Linux 5.8.0-63-generic x86_64
```

I found a vulnerable version of redis, this will lead to RCE on the target system ->

https://github.com/n0b0dyCN/redis-rogue-server

![Pasted image 20240610223224.png](Evidence/Pasted%20image%2020240610223224.png)

![Pasted image 20240610223247.png](Evidence/Pasted%20image%2020240610223247.png)

Got my a reverse shell back, Time to upgrade my shell, and start enumeration.

