## Host Info
```
TARGET

OS details: Linux 2.6.18
```


## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Fri Jun 21 08:57:24 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.063s latency).
Scanned at 2024-06-21 08:57:24 EDT for 18s
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 61 OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
| ssh-hostkey: 
|   3072 c9:c3:da:15:28:3b:f1:f8:9a:36:df:4d:36:6b:a7:44 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDNEbgprJqVJa8R95Wkbo3cemB4fdRzos+v750LtPEnRs+IJQn5jcg5l89Tx4junU+AXzLflrMVo55gbuKeNTDtFRU9ltlIu4AU+f7lRlUlvAHlNjUbU/z3WBZ5ZU9j7Xc9WKjh1Ov7chC0UnDdyr5EGrIwlLzgk8zrWx364+S4JqLtER2/n0rhVxa9RCw0tR/oL24kMep4q7rFK6dThiRtQ9nsJFhh6yw8Fmdg7r4uohqH70UJurVwVNwFqtr/86e4VSSoITlMQPZrZFVvoSsjyL8LEODt1qznoLWudMD95Eo1YFSPID5VcS0kSElfYigjSr+9bNSdlzAof1mU6xJA67BggGNu6qITWWIJySXcropehnDAt2nv4zaKAUKc/T0ij9wkIBskuXfN88cEmZbu+gObKbLgwQSRQJIpQ+B/mA8CD4AiaTmEwGSWz1dVPp5Fgb6YVy6E4oO9ASuD9Q1JWuRmnn8uiHF/nPLs2LC2+rh3nPLXlV+MG/zUfQCrdrE=
|   256 26:03:2b:f6:da:90:1d:1b:ec:8d:8f:8d:1e:7e:3d:6b (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBCUhhvrIBs53SApXKZYHWBlpH50KO3POt8Y+WvTvHZ5YgRagAEU5eSnGkrnziCUvDWNShFhLHI7kQv+mx+4R6Wk=
|   256 fb:43:b2:b0:19:2f:d3:f6:bc:aa:60:67:ab:c1:af:37 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIN4MSEXnpONsc0ANUT6rFQPWsoVmRW4hrpSRq++xySM9
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
|_http-favicon: Unknown favicon MD5: 2D58FC0104110AF4C9BE979DFD8FD83C
|_http-title: PluXml - Blog or CMS, XML powered !
|_http-server-header: Apache/2.4.56 (Debian)
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
Device type: general purpose|storage-misc|firewall
Running (JUST GUESSING): Linux 2.6.X|3.X|4.X (85%), Synology DiskStation Manager 5.X (85%), WatchGuard Fireware 11.X (85%)
OS CPE: cpe:/o:linux:linux_kernel:2.6.32 cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:4.4 cpe:/o:linux:linux_kernel cpe:/a:synology:diskstation_manager:5.1 cpe:/o:watchguard:fireware:11.8
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Linux 2.6.32 (85%), Linux 2.6.39 (85%), Linux 3.10 - 3.12 (85%), Linux 3.4 (85%), Linux 3.5 (85%), Linux 4.4 (85%), Synology DiskStation Manager 5.1 (85%), WatchGuard Fireware 11.8 (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=6/21%OT=22%CT=1%CU=%PV=Y%DS=4%DC=T%G=N%TM=667578C6%P=x86_64-pc-linux-gnu)
SEQ(SP=105%GCD=1%ISR=10C%TI=Z%TS=A)
OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)
WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)
ECN(R=Y%DF=Y%TG=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)
T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
T5(R=N)
T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=N)
T7(R=N)
U1(R=N)
IE(R=Y%DFI=N%TG=40%CD=S)

Uptime guess: 21.164 days (since Fri May 31 05:01:52 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=261 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 256/tcp)
HOP RTT      ADDRESS
1   63.77 ms ATTACKER
2   63.63 ms ATTACKER
3   63.79 ms TARGET
4   64.09 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Jun 21 08:57:42 2024 -- 1 IP address (1 host up) scanned in 18.23 seconds

```

#### Full Scan
```

# Nmap 7.94SVN scan initiated Fri Jun 21 08:57:24 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -198180 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -198180 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -266657 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -266657 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -194642 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -194642 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -254289 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -254289 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -196872 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -196872 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -319371 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -319371 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -192210 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -192210 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-06-21 08:57:24 EDT for 76s
Not shown: 65533 closed tcp ports (reset)
PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 61 OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
| ssh-hostkey: 
|   3072 c9:c3:da:15:28:3b:f1:f8:9a:36:df:4d:36:6b:a7:44 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDNEbgprJqVJa8R95Wkbo3cemB4fdRzos+v750LtPEnRs+IJQn5jcg5l89Tx4junU+AXzLflrMVo55gbuKeNTDtFRU9ltlIu4AU+f7lRlUlvAHlNjUbU/z3WBZ5ZU9j7Xc9WKjh1Ov7chC0UnDdyr5EGrIwlLzgk8zrWx364+S4JqLtER2/n0rhVxa9RCw0tR/oL24kMep4q7rFK6dThiRtQ9nsJFhh6yw8Fmdg7r4uohqH70UJurVwVNwFqtr/86e4VSSoITlMQPZrZFVvoSsjyL8LEODt1qznoLWudMD95Eo1YFSPID5VcS0kSElfYigjSr+9bNSdlzAof1mU6xJA67BggGNu6qITWWIJySXcropehnDAt2nv4zaKAUKc/T0ij9wkIBskuXfN88cEmZbu+gObKbLgwQSRQJIpQ+B/mA8CD4AiaTmEwGSWz1dVPp5Fgb6YVy6E4oO9ASuD9Q1JWuRmnn8uiHF/nPLs2LC2+rh3nPLXlV+MG/zUfQCrdrE=
|   256 26:03:2b:f6:da:90:1d:1b:ec:8d:8f:8d:1e:7e:3d:6b (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBCUhhvrIBs53SApXKZYHWBlpH50KO3POt8Y+WvTvHZ5YgRagAEU5eSnGkrnziCUvDWNShFhLHI7kQv+mx+4R6Wk=
|   256 fb:43:b2:b0:19:2f:d3:f6:bc:aa:60:67:ab:c1:af:37 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIN4MSEXnpONsc0ANUT6rFQPWsoVmRW4hrpSRq++xySM9
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
|_http-favicon: Unknown favicon MD5: 2D58FC0104110AF4C9BE979DFD8FD83C
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-title: PluXml - Blog or CMS, XML powered !
|_http-server-header: Apache/2.4.56 (Debian)
Aggressive OS guesses: Linux 2.6.32 (87%), Linux 2.6.32 or 3.10 (87%), Linux 3.5 (87%), Synology DiskStation Manager 5.1 (87%), Linux 2.6.35 (87%), Linux 2.6.39 (86%), Linux 3.10 - 3.12 (86%), Linux 4.2 (86%), Linux 4.4 (86%), WatchGuard Fireware 11.8 (86%)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=6/21%OT=22%CT=1%CU=37445%PV=Y%DS=4%DC=T%G=Y%TM=6675
OS:7900%P=x86_64-pc-linux-gnu)SEQ(SP=FF%GCD=1%ISR=103%TI=Z%TS=A)SEQ(SP=FF%G
OS:CD=1%ISR=104%TI=Z%TS=A)OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11NW7
OS:%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)WIN(W1=FE88%W2=FE88%W3=FE88%W
OS:4=FE88%W5=FE88%W6=FE88)ECN(R=Y%DF=Y%T=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)T1(
OS:R=Y%DF=Y%T=40%S=O%A=S+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(R=N)T5(R=Y%DF=Y%T=4
OS:0%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=N)T7(R=N)U1(R=Y%DF=N%T=40%IPL=164%UN
OS:=0%RIPL=G%RID=G%RIPCK=G%RUCK=AC89%RUD=G)IE(R=Y%DFI=N%T=40%CD=S)

Uptime guess: 21.164 days (since Fri May 31 05:01:52 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=255 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 21/tcp)
HOP RTT      ADDRESS
1   58.51 ms ATTACKER
2   58.46 ms ATTACKER
3   58.52 ms TARGET
4   58.62 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Jun 21 08:58:40 2024 -- 1 IP address (1 host up) scanned in 76.15 seconds

```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Fri Jun 21 08:57:24 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/... -oX /home/kali/... TARGET
Warning: TARGET giving up on port because retransmission cap hit (6).
Increasing send delay for TARGET from 100 to 200 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for TARGET from 200 to 400 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for TARGET from 400 to 800 due to 11 out of 11 dropped probes since last increase.
adjust_timeouts2: packet supposedly had rtt of -88633 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.064s latency).
Scanned at 2024-06-21 08:57:24 EDT for 231s
Not shown: 78 closed udp ports (port-unreach)
PORT      STATE         SERVICE        REASON      VERSION
7/udp     open|filtered echo           no-response
17/udp    open|filtered qotd           no-response
53/udp    open|filtered domain         no-response
67/udp    open|filtered dhcps          no-response
69/udp    open|filtered tftp           no-response
80/udp    open|filtered http           no-response
111/udp   open|filtered rpcbind        no-response
161/udp   open|filtered snmp           no-response
162/udp   open|filtered snmptrap       no-response
497/udp   open|filtered retrospect     no-response
500/udp   open|filtered isakmp         no-response
626/udp   open|filtered serialnumberd  no-response
997/udp   open|filtered maitrd         no-response
1029/udp  open|filtered solid-mux      no-response
2223/udp  open|filtered rockwell-csp2  no-response
5632/udp  open|filtered pcanywherestat no-response
31337/udp open|filtered BackOrifice    no-response
32769/udp open|filtered filenet-rpc    no-response
49154/udp open|filtered unknown        no-response
49182/udp open|filtered unknown        no-response
49193/udp open|filtered unknown        no-response
49201/udp open|filtered unknown        no-response
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.18
OS details: Linux 2.6.18, Linux 2.6.30
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=6/21%OT=%CT=%CU=9%PV=Y%DS=4%DC=T%G=N%TM=6675799B%P=
OS:x86_64-pc-linux-gnu)SEQ()T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U
OS:1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=4CD1%RUD=G)IE(R=Y
OS:%DFI=N%T=40%CD=S)

Network Distance: 4 hops

TRACEROUTE (using port 445/udp)
HOP RTT      ADDRESS
1   57.52 ms ATTACKER
2   57.55 ms ATTACKER
3   58.29 ms TARGET
4   60.56 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Jun 21 09:01:15 2024 -- 1 IP address (1 host up) scanned in 231.38 seconds


```

