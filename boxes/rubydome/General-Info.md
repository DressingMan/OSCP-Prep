## Host Info
```bash
TARGET

Linux
```


## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Fri Jul 12 15:15:11 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -1818626 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -1818626 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.26s latency).
Scanned at 2024-07-12 15:15:11 EDT for 61s
Not shown: 998 closed tcp ports (reset)
PORT     STATE SERVICE REASON         VERSION
22/tcp   open  ssh     syn-ack ttl 61 OpenSSH 8.9p1 Ubuntu 3ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 b9:bc:8f:01:3f:85:5d:f9:5c:d9:fb:b6:15:a0:1e:74 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBBYESg2KmNLhFh1KJaN2UFCVAEv6MWr58pqp2fIpCSBEK2wDJ5ap2XVBVGLk9Po4eKBbqTo96yttfVUvXWXoN3M=
|   256 53:d9:7f:3d:22:8a:fd:57:98:fe:6b:1a:4c:ac:79:67 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIBdIs4PWZ8yY2OQ6Jlk84Ihd5+15Nb3l0qvpf1ls3wfa
3000/tcp open  http    syn-ack ttl 61 WEBrick httpd 1.7.0 (Ruby 3.0.2 (2021-07-07))
|_http-title: RubyDome HTML to PDF
| http-methods: 
|_  Supported Methods: GET HEAD
|_http-server-header: WEBrick/1.7.0 (Ruby/3.0.2/2021-07-07)
OS fingerprint not ideal because: maxTimingRatio (2.808000e+00) is greater than 1.4
Aggressive OS guesses: Linux 2.6.32 (87%), Linux 2.6.32 or 3.10 (87%), Linux 3.5 (87%), Linux 4.2 (87%), Linux 4.4 (87%), Synology DiskStation Manager 5.1 (87%), WatchGuard Fireware 11.8 (87%), Linux 2.6.35 (87%), Linux 2.6.39 (86%), Linux 3.10 - 3.12 (86%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=7/12%OT=22%CT=1%CU=32768%PV=Y%DS=4%DC=T%G=N%TM=669180FC%P=x86_64-pc-linux-gnu)
SEQ(SP=101%GCD=1%ISR=106%TI=Z%TS=8)
SEQ(SP=101%GCD=1%ISR=106%TI=Z%TS=A)
SEQ(SP=101%GCD=1%ISR=106%TI=Z%II=I%TS=1)
SEQ(SP=101%GCD=1%ISR=106%TI=Z%II=I%TS=A)
SEQ(SP=103%GCD=1%ISR=104%TI=Z%TS=9)
OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)
WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)
ECN(R=Y%DF=Y%T=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)
T1(R=Y%DF=Y%T=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=N)
T7(R=N)
U1(R=N)
U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=8D95%RUD=G)
IE(R=Y%DFI=N%T=40%CD=S)

Uptime guess: 88.618 days (since Mon Apr 15 00:26:44 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=259 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 256/tcp)
HOP RTT       ADDRESS
1   155.45 ms ATTACKER
2   155.33 ms ATTACKER
3   155.90 ms TARGET
4   155.99 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Jul 12 15:16:12 2024 -- 1 IP address (1 host up) scanned in 61.80 seconds

```

#### Full Scan
```bash

# Nmap 7.94SVN scan initiated Fri Jul 12 15:15:11 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
Warning: TARGET giving up on port because retransmission cap hit (6).
adjust_timeouts2: packet supposedly had rtt of -135548 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -135548 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -166244 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -166244 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -192022 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -192022 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -187387 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -187387 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -106802 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -106802 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.11s latency).
Scanned at 2024-07-12 15:15:11 EDT for 1079s
Not shown: 65497 closed tcp ports (reset)
PORT      STATE    SERVICE   REASON         VERSION
22/tcp    open     ssh       syn-ack ttl 61 OpenSSH 8.9p1 Ubuntu 3ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 b9:bc:8f:01:3f:85:5d:f9:5c:d9:fb:b6:15:a0:1e:74 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBBYESg2KmNLhFh1KJaN2UFCVAEv6MWr58pqp2fIpCSBEK2wDJ5ap2XVBVGLk9Po4eKBbqTo96yttfVUvXWXoN3M=
|   256 53:d9:7f:3d:22:8a:fd:57:98:fe:6b:1a:4c:ac:79:67 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIBdIs4PWZ8yY2OQ6Jlk84Ihd5+15Nb3l0qvpf1ls3wfa
3000/tcp  open     http      syn-ack ttl 61 WEBrick httpd 1.7.0 (Ruby 3.0.2 (2021-07-07))
|_http-title: RubyDome HTML to PDF
| http-methods: 
|_  Supported Methods: GET HEAD
|_http-server-header: WEBrick/1.7.0 (Ruby/3.0.2/2021-07-07)
4310/tcp  filtered mirrtex   no-response
4342/tcp  filtered lisp-cons no-response
4856/tcp  filtered unknown   no-response
7033/tcp  filtered unknown   no-response
7790/tcp  filtered unknown   no-response
9084/tcp  filtered aurora    no-response
10983/tcp filtered unknown   no-response
11024/tcp filtered unknown   no-response
13070/tcp filtered unknown   no-response
14951/tcp filtered unknown   no-response
21282/tcp filtered unknown   no-response
21906/tcp filtered unknown   no-response
26366/tcp filtered unknown   no-response
27067/tcp filtered unknown   no-response
28754/tcp filtered unknown   no-response
30870/tcp filtered unknown   no-response
30956/tcp filtered unknown   no-response
32624/tcp filtered unknown   no-response
32870/tcp filtered unknown   no-response
35757/tcp filtered unknown   no-response
39686/tcp filtered unknown   no-response
41051/tcp filtered unknown   no-response
41715/tcp filtered unknown   no-response
45372/tcp filtered unknown   no-response
47684/tcp filtered unknown   no-response
49150/tcp filtered inspider  no-response
49368/tcp filtered unknown   no-response
50473/tcp filtered unknown   no-response
50614/tcp filtered unknown   no-response
51432/tcp filtered unknown   no-response
52919/tcp filtered unknown   no-response
55768/tcp filtered unknown   no-response
57192/tcp filtered unknown   no-response
57998/tcp filtered unknown   no-response
60594/tcp filtered unknown   no-response
61523/tcp filtered unknown   no-response
Aggressive OS guesses: Linux 2.6.32 (88%), Linux 2.6.39 (88%), Linux 3.10 - 3.12 (88%), Linux 3.4 (88%), Linux 3.5 (88%), Linux 4.2 (88%), Linux 4.4 (88%), Synology DiskStation Manager 5.1 (88%), WatchGuard Fireware 11.8 (88%), Linux 2.6.35 (87%)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=7/12%OT=22%CT=1%CU=38210%PV=Y%DS=4%DC=T%G=Y%TM=6691
OS:84F6%P=x86_64-pc-linux-gnu)SEQ(SP=105%GCD=1%ISR=10B%TI=Z%TS=A)SEQ(SP=105
OS:%GCD=1%ISR=10B%TI=Z%II=I%TS=A)OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551N
OS:NT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)WIN(W1=FE88%W2=FE88%W3
OS:=FE88%W4=FE88%W5=FE88%W6=FE88)ECN(R=Y%DF=Y%T=40%W=FAF0%O=M551NNSNW7%CC=Y
OS:%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(R=N)T5(R=Y%D
OS:F=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=N)T7(R=N)U1(R=Y%DF=N%T=40%IPL
OS:=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=A98D%RUD=G)IE(R=Y%DFI=N%T=40%CD=S)

Uptime guess: 43.169 days (since Thu May 30 11:30:13 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=261 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 1723/tcp)
HOP RTT       ADDRESS
1   393.78 ms ATTACKER
2   393.83 ms ATTACKER
3   394.04 ms TARGET
4   395.80 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Jul 12 15:33:10 2024 -- 1 IP address (1 host up) scanned in 1079.39 seconds

```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Fri Jul 12 15:15:11 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/... -oX /home/kali/... TARGET
Warning: TARGET giving up on port because retransmission cap hit (6).
Increasing send delay for TARGET from 100 to 200 due to 11 out of 13 dropped probes since last increase.
Increasing send delay for TARGET from 200 to 400 due to 11 out of 13 dropped probes since last increase.
Increasing send delay for TARGET from 400 to 800 due to 11 out of 18 dropped probes since last increase.
Nmap scan report for TARGET
Host is up, received user-set (0.24s latency).
Scanned at 2024-07-12 15:15:12 EDT for 211s
Not shown: 89 closed udp ports (port-unreach)
PORT      STATE         SERVICE         REASON      VERSION
88/udp    open|filtered kerberos-sec    no-response
445/udp   open|filtered microsoft-ds    no-response
1719/udp  open|filtered h323gatestat    no-response
3283/udp  open|filtered netassistant    no-response
4500/udp  open|filtered nat-t-ike       no-response
10000/udp open|filtered ndmp            no-response
20031/udp open|filtered bakbonenetvault no-response
32768/udp open|filtered omad            no-response
33281/udp open|filtered unknown         no-response
49153/udp open|filtered unknown         no-response
49182/udp open|filtered unknown         no-response
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.18
OS details: Linux 2.6.18, Linux 2.6.30
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=7/12%OT=%CT=%CU=7%PV=Y%DS=4%DC=T%G=N%TM=66918193%P=
OS:x86_64-pc-linux-gnu)SEQ(II=I)SEQ(II=RI)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=A
OS:R%O=%RD=0%Q=)U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=E4F
OS:2%RUD=G)IE(R=Y%DFI=N%T=40%CD=S)

Network Distance: 4 hops

TRACEROUTE (using port 1718/udp)
HOP RTT       ADDRESS
1   453.76 ms ATTACKER
2   453.86 ms ATTACKER
3   453.89 ms TARGET
4   216.88 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Jul 12 15:18:43 2024 -- 1 IP address (1 host up) scanned in 212.20 seconds


```

