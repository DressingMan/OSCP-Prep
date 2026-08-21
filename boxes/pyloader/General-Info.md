## Host Info
```bash
TARGET

Identified HTTP Server: Cheroot/8.6.0

```


## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Mon Jul 15 22:05:45 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.069s latency).
Scanned at 2024-07-15 22:05:46 EDT for 48s
Not shown: 998 closed tcp ports (reset)
PORT     STATE SERVICE REASON         VERSION
22/tcp   open  ssh     syn-ack ttl 61 OpenSSH 8.9p1 Ubuntu 3ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 b9:bc:8f:01:3f:85:5d:f9:5c:d9:fb:b6:15:a0:1e:74 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBBYESg2KmNLhFh1KJaN2UFCVAEv6MWr58pqp2fIpCSBEK2wDJ5ap2XVBVGLk9Po4eKBbqTo96yttfVUvXWXoN3M=
|   256 53:d9:7f:3d:22:8a:fd:57:98:fe:6b:1a:4c:ac:79:67 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIBdIs4PWZ8yY2OQ6Jlk84Ihd5+15Nb3l0qvpf1ls3wfa
9666/tcp open  http    syn-ack ttl 61 CherryPy wsgiserver
|_http-favicon: Unknown favicon MD5: 71AAC1BA3CF57C009DA1994F94A2CC89
| http-methods: 
|_  Supported Methods: OPTIONS GET HEAD
|_http-server-header: Cheroot/8.6.0
| http-title: Login - pyLoad 
|_Requested resource was /login?next=http://TARGET:9666/
| http-robots.txt: 1 disallowed entry 
|_/
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
No OS matches for host
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=7/15%OT=22%CT=1%CU=%PV=Y%DS=4%DC=T%G=N%TM=6695D5AA%P=x86_64-pc-linux-gnu)
SEQ(SP=106%GCD=1%ISR=10B%TI=Z%TS=A)
SEQ(SP=106%GCD=1%ISR=10C%TI=Z%TS=A)
OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)
WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)
ECN(R=N)
T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
T5(R=N)
T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=N)
T7(R=N)
U1(R=N)
IE(R=N)
IE(R=Y%DFI=N%TG=40%CD=S)

Uptime guess: 5.012 days (since Wed Jul 10 21:48:43 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=262 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 23/tcp)
HOP RTT      ADDRESS
1   67.99 ms ATTACKER
2   67.91 ms ATTACKER
3   70.12 ms TARGET
4   70.46 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul 15 22:06:34 2024 -- 1 IP address (1 host up) scanned in 49.11 seconds

```

#### Full Scan
```bash


```

#### UDP scan
```bash

# Nmap 7.94SVN scan initiated Mon Jul 15 22:05:45 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/... -oX /home/kali/... TARGET
Warning: TARGET giving up on port because retransmission cap hit (6).
Increasing send delay for TARGET from 100 to 200 due to 11 out of 13 dropped probes since last increase.
Increasing send delay for TARGET from 200 to 400 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for TARGET from 400 to 800 due to 11 out of 11 dropped probes since last increase.
Nmap scan report for TARGET
Host is up, received user-set (0.14s latency).
Scanned at 2024-07-15 22:05:46 EDT for 200s
Not shown: 91 closed udp ports (port-unreach)
PORT      STATE         SERVICE REASON      VERSION
7/udp     open|filtered echo    no-response
9/udp     open|filtered discard no-response
120/udp   open|filtered cfdptkt no-response
998/udp   open|filtered puparp  no-response
1030/udp  open|filtered iad1    no-response
1646/udp  open|filtered radacct no-response
9200/udp  open|filtered wap-wsp no-response
32768/udp open|filtered omad    no-response
49188/udp open|filtered unknown no-response
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.18
OS details: Linux 2.6.18, Linux 2.6.30
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=7/15%OT=%CT=%CU=17%PV=Y%DS=4%DC=T%G=N%TM=6695D642%P
OS:=x86_64-pc-linux-gnu)SEQ(II=I)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0
OS:%Q=)U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=3D26%RUD=G)I
OS:E(R=Y%DFI=N%T=40%CD=S)

Network Distance: 4 hops

TRACEROUTE (using port 138/udp)
HOP RTT      ADDRESS
1   68.03 ms ATTACKER
2   68.06 ms ATTACKER
3   68.11 ms TARGET
4   68.16 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul 15 22:09:06 2024 -- 1 IP address (1 host up) scanned in 201.31 seconds

```

