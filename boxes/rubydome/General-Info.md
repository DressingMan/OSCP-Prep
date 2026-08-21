## Host Info
```bash
TARGET

Linux
```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Fri Jul 12 15:15:11 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.26s latency).
Scanned at 2024-07-12 15:15:11 EDT for 61s
Not shown: 998 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.9p1 Ubuntu 3ubuntu0.1 (Ubuntu Linux; protocol 2.0)
3000/tcp open http WEBrick httpd 1.7.0 (Ruby 3.0.2 (2021-07-07))
|_http-title: RubyDome HTML to PDF
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Fri Jul 12 15:16:12 2024 -- 1 IP address (1 host up) scanned in 61.80 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Fri Jul 12 15:15:11 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.11s latency).
Scanned at 2024-07-12 15:15:11 EDT for 1079s
Not shown: 65497 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.9p1 Ubuntu 3ubuntu0.1 (Ubuntu Linux; protocol 2.0)
3000/tcp open http WEBrick httpd 1.7.0 (Ruby 3.0.2 (2021-07-07))
|_http-title: RubyDome HTML to PDF
4310/tcp filtered mirrtex no-response
4342/tcp filtered lisp-cons no-response
4856/tcp filtered unknown no-response
7033/tcp filtered unknown no-response
7790/tcp filtered unknown no-response
9084/tcp filtered aurora no-response
10983/tcp filtered unknown no-response
11024/tcp filtered unknown no-response
13070/tcp filtered unknown no-response
14951/tcp filtered unknown no-response
21282/tcp filtered unknown no-response
21906/tcp filtered unknown no-response
26366/tcp filtered unknown no-response
27067/tcp filtered unknown no-response
28754/tcp filtered unknown no-response
30870/tcp filtered unknown no-response
30956/tcp filtered unknown no-response
32624/tcp filtered unknown no-response
32870/tcp filtered unknown no-response
35757/tcp filtered unknown no-response
39686/tcp filtered unknown no-response
41051/tcp filtered unknown no-response
41715/tcp filtered unknown no-response
45372/tcp filtered unknown no-response
47684/tcp filtered unknown no-response
49150/tcp filtered inspider no-response
49368/tcp filtered unknown no-response
50473/tcp filtered unknown no-response
50614/tcp filtered unknown no-response
51432/tcp filtered unknown no-response
```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Fri Jul 12 15:15:11 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.24s latency).
Scanned at 2024-07-12 15:15:12 EDT for 211s
Not shown: 89 closed udp ports (port-unreach)
PORT      STATE SERVICE        VERSION
# Nmap done at Fri Jul 12 15:18:43 2024 -- 1 IP address (1 host up) scanned in 212.20 seconds
# UDP: 11 open|filtered omitted (none confirmed open)
```

