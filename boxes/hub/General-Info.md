## Host Info
```
TARGET
```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Mon Jul  1 17:33:05 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.072s latency).
Scanned at 2024-07-01 17:33:10 EDT for 33s
Not shown: 996 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http nginx 1.18.0
|_http-title: 403 Forbidden
8082/tcp open http Barracuda Embedded Web Server
|_http-title: Home
| http-methods:
|_  Potentially risky methods: PROPFIND PATCH PUT COPY DELETE MOVE MKCOL PROPPATCH LOCK UNLOCK
9999/tcp open ssl/http Barracuda Embedded Web Server
| ssl-cert: Subject: commonName=FuguHub/stateOrProvinceName=California/countryName=US
| http-methods:
|_  Potentially risky methods: PROPFIND PATCH PUT COPY DELETE MOVE MKCOL PROPPATCH LOCK UNLOCK
|_http-title: Home
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Jul  1 17:33:43 2024 -- 1 IP address (1 host up) scanned in 37.85 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Mon Jul  1 17:33:05 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.095s latency).
Scanned at 2024-07-01 17:33:06 EDT for 878s
Not shown: 65495 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http nginx 1.18.0
|_http-title: 403 Forbidden
1263/tcp filtered dka no-response
2718/tcp filtered pn-requester2 no-response
4450/tcp filtered camp no-response
8082/tcp open http Barracuda Embedded Web Server
| http-methods:
|_  Potentially risky methods: PROPFIND PATCH PUT COPY DELETE MOVE MKCOL PROPPATCH LOCK UNLOCK
9999/tcp open ssl/http Barracuda Embedded Web Server
| ssl-cert: Subject: commonName=FuguHub/stateOrProvinceName=California/countryName=US
|_http-title: Home
14750/tcp filtered unknown no-response
17339/tcp filtered unknown no-response
19932/tcp filtered unknown no-response
23826/tcp filtered unknown no-response
26537/tcp filtered unknown no-response
27121/tcp filtered unknown no-response
27577/tcp filtered unknown no-response
28306/tcp filtered unknown no-response
30750/tcp filtered unknown no-response
31890/tcp filtered unknown no-response
33095/tcp filtered unknown no-response
33797/tcp filtered unknown no-response
34195/tcp filtered unknown no-response
34927/tcp filtered unknown no-response
39268/tcp filtered unknown no-response
39433/tcp filtered unknown no-response
39721/tcp filtered unknown no-response
```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Mon Jul  1 17:33:05 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.17s latency).
Scanned at 2024-07-01 17:33:10 EDT for 254s
Not shown: 83 closed udp ports (port-unreach)
PORT      STATE SERVICE        VERSION
# Nmap done at Mon Jul  1 17:37:24 2024 -- 1 IP address (1 host up) scanned in 259.64 seconds
# UDP: 17 open|filtered omitted (none confirmed open)
```

