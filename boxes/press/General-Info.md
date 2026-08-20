## Host Info
```

 TARGET


```


## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Mon Oct 21 15:59:14 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -438350 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -438350 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -737107 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -737107 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-10-21 15:59:15 EDT for 24s
Not shown: 997 closed tcp ports (reset)
PORT     STATE SERVICE REASON         VERSION
22/tcp   open  ssh     syn-ack ttl 61 OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
| ssh-hostkey: 
|   3072 c9:c3:da:15:28:3b:f1:f8:9a:36:df:4d:36:6b:a7:44 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDNEbgprJqVJa8R95Wkbo3cemB4fdRzos+v750LtPEnRs+IJQn5jcg5l89Tx4junU+AXzLflrMVo55gbuKeNTDtFRU9ltlIu4AU+f7lRlUlvAHlNjUbU/z3WBZ5ZU9j7Xc9WKjh1Ov7chC0UnDdyr5EGrIwlLzgk8zrWx364+S4JqLtER2/n0rhVxa9RCw0tR/oL24kMep4q7rFK6dThiRtQ9nsJFhh6yw8Fmdg7r4uohqH70UJurVwVNwFqtr/86e4VSSoITlMQPZrZFVvoSsjyL8LEODt1qznoLWudMD95Eo1YFSPID5VcS0kSElfYigjSr+9bNSdlzAof1mU6xJA67BggGNu6qITWWIJySXcropehnDAt2nv4zaKAUKc/T0ij9wkIBskuXfN88cEmZbu+gObKbLgwQSRQJIpQ+B/mA8CD4AiaTmEwGSWz1dVPp5Fgb6YVy6E4oO9ASuD9Q1JWuRmnn8uiHF/nPLs2LC2+rh3nPLXlV+MG/zUfQCrdrE=
|   256 26:03:2b:f6:da:90:1d:1b:ec:8d:8f:8d:1e:7e:3d:6b (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBCUhhvrIBs53SApXKZYHWBlpH50KO3POt8Y+WvTvHZ5YgRagAEU5eSnGkrnziCUvDWNShFhLHI7kQv+mx+4R6Wk=
|   256 fb:43:b2:b0:19:2f:d3:f6:bc:aa:60:67:ab:c1:af:37 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIN4MSEXnpONsc0ANUT6rFQPWsoVmRW4hrpSRq++xySM9
80/tcp   open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
|_http-title: Lugx Gaming Shop HTML5 Template
|_http-server-header: Apache/2.4.56 (Debian)
| http-methods: 
|_  Supported Methods: OPTIONS HEAD GET POST
8089/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-generator: FlatPress fp-1.2.1
|_http-favicon: Unknown favicon MD5: 315957B26C1BD8805590E36985990754
|_http-title: FlatPress
|_http-server-header: Apache/2.4.56 (Debian)
Device type: general purpose|storage-misc|firewall
Running (JUST GUESSING): Linux 2.6.X|3.X|4.X (85%), Synology DiskStation Manager 5.X (85%), WatchGuard Fireware 11.X (85%)
OS CPE: cpe:/o:linux:linux_kernel:2.6.32 cpe:/o:linux:linux_kernel:3.10 cpe:/o:linux:linux_kernel:4.2 cpe:/o:linux:linux_kernel cpe:/a:synology:diskstation_manager:5.1 cpe:/o:watchguard:fireware:11.8
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Linux 2.6.32 (85%), Linux 2.6.32 or 3.10 (85%), Linux 2.6.39 (85%), Linux 3.10 - 3.12 (85%), Linux 3.4 (85%), Linux 3.5 (85%), Linux 4.2 (85%), Linux 4.4 (85%), Synology DiskStation Manager 5.1 (85%), WatchGuard Fireware 11.8 (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=10/21%OT=22%CT=1%CU=%PV=Y%DS=4%DC=T%G=N%TM=6716B2AB%P=x86_64-pc-linux-gnu)
SEQ(SP=103%GCD=1%ISR=10A%TI=Z%TS=A)
OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)
WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)
ECN(R=Y%DF=Y%TG=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)
T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=N)
T7(R=N)
U1(R=N)
IE(R=Y%DFI=N%TG=40%CD=S)

Uptime guess: 39.297 days (since Thu Sep 12 08:51:45 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=259 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 995/tcp)
HOP RTT      ADDRESS
1   58.71 ms ATTACKER
2   58.69 ms ATTACKER
3   62.66 ms TARGET
4   65.34 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Oct 21 15:59:39 2024 -- 1 IP address (1 host up) scanned in 25.05 seconds

```

#### Full Scan
```bash

# Nmap 7.94SVN scan initiated Mon Oct 21 15:59:14 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -447304 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -447304 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -870368 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -870368 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -725810 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -725810 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -467350 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -467350 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -462843 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -462843 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -457697 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -457697 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -707444 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -707444 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.057s latency).
Scanned at 2024-10-21 15:59:15 EDT for 70s
Not shown: 65532 closed tcp ports (reset)
PORT     STATE SERVICE REASON         VERSION
22/tcp   open  ssh     syn-ack ttl 61 OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
| ssh-hostkey: 
|   3072 c9:c3:da:15:28:3b:f1:f8:9a:36:df:4d:36:6b:a7:44 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDNEbgprJqVJa8R95Wkbo3cemB4fdRzos+v750LtPEnRs+IJQn5jcg5l89Tx4junU+AXzLflrMVo55gbuKeNTDtFRU9ltlIu4AU+f7lRlUlvAHlNjUbU/z3WBZ5ZU9j7Xc9WKjh1Ov7chC0UnDdyr5EGrIwlLzgk8zrWx364+S4JqLtER2/n0rhVxa9RCw0tR/oL24kMep4q7rFK6dThiRtQ9nsJFhh6yw8Fmdg7r4uohqH70UJurVwVNwFqtr/86e4VSSoITlMQPZrZFVvoSsjyL8LEODt1qznoLWudMD95Eo1YFSPID5VcS0kSElfYigjSr+9bNSdlzAof1mU6xJA67BggGNu6qITWWIJySXcropehnDAt2nv4zaKAUKc/T0ij9wkIBskuXfN88cEmZbu+gObKbLgwQSRQJIpQ+B/mA8CD4AiaTmEwGSWz1dVPp5Fgb6YVy6E4oO9ASuD9Q1JWuRmnn8uiHF/nPLs2LC2+rh3nPLXlV+MG/zUfQCrdrE=
|   256 26:03:2b:f6:da:90:1d:1b:ec:8d:8f:8d:1e:7e:3d:6b (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBCUhhvrIBs53SApXKZYHWBlpH50KO3POt8Y+WvTvHZ5YgRagAEU5eSnGkrnziCUvDWNShFhLHI7kQv+mx+4R6Wk=
|   256 fb:43:b2:b0:19:2f:d3:f6:bc:aa:60:67:ab:c1:af:37 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIN4MSEXnpONsc0ANUT6rFQPWsoVmRW4hrpSRq++xySM9
80/tcp   open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
|_http-title: Lugx Gaming Shop HTML5 Template
|_http-server-header: Apache/2.4.56 (Debian)
| http-methods: 
|_  Supported Methods: OPTIONS HEAD GET POST
8089/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
|_http-server-header: Apache/2.4.56 (Debian)
|_http-title: FlatPress
|_http-generator: FlatPress fp-1.2.1
|_http-favicon: Unknown favicon MD5: 315957B26C1BD8805590E36985990754
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
Aggressive OS guesses: Linux 2.6.32 (87%), Linux 2.6.32 or 3.10 (87%), Linux 2.6.39 (87%), Linux 3.10 - 3.12 (87%), Linux 3.4 (87%), Linux 4.4 (87%), Synology DiskStation Manager 5.1 (87%), WatchGuard Fireware 11.8 (87%), Linux 2.6.35 (87%), Linux 3.10 (87%)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=10/21%OT=22%CT=1%CU=34002%PV=Y%DS=4%DC=T%G=Y%TM=671
OS:6B2D9%P=x86_64-pc-linux-gnu)SEQ(SP=102%GCD=1%ISR=10D%TI=Z%TS=A)SEQ(SP=10
OS:3%GCD=1%ISR=10D%TI=Z%TS=A)OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11
OS:NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)WIN(W1=FE88%W2=FE88%W3=FE8
OS:8%W4=FE88%W5=FE88%W6=FE88)ECN(R=Y%DF=Y%TG=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=
OS:)ECN(R=Y%DF=Y%T=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)T1(R=Y%DF=Y%TG=40%S=O%A=S
OS:+%F=AS%RD=0%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(R
OS:=N)T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T5(R=Y%DF=Y%T=40%W=0%S
OS:=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=N)T7(R=N)U1(R=N)U1(R=Y%DF=N%T=40%IPL=164%UN
OS:=0%RIPL=G%RID=G%RIPCK=G%RUCK=86E1%RUD=G)IE(R=Y%DFI=N%TG=40%CD=S)IE(R=Y%D
OS:FI=N%T=40%CD=S)

Uptime guess: 39.298 days (since Thu Sep 12 08:51:45 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=258 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 3389/tcp)
HOP RTT      ADDRESS
1   56.21 ms ATTACKER
2   56.16 ms ATTACKER
3   58.95 ms TARGET
4   59.05 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Oct 21 16:00:25 2024 -- 1 IP address (1 host up) scanned in 71.07 seconds

```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Mon Oct 21 15:59:14 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/... -oX /home/kali/... TARGET
Increasing send delay for TARGET from 50 to 100 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for TARGET from 100 to 200 due to 11 out of 12 dropped probes since last increase.
Increasing send delay for TARGET from 200 to 400 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for TARGET from 400 to 800 due to 11 out of 11 dropped probes since last increase.
adjust_timeouts2: packet supposedly had rtt of -410182 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.057s latency).
Scanned at 2024-10-21 15:59:15 EDT for 307s

PORT      STATE         SERVICE         REASON              VERSION
7/udp     closed        echo            port-unreach ttl 61
9/udp     closed        discard         port-unreach ttl 61
17/udp    closed        qotd            port-unreach ttl 61
19/udp    closed        chargen         port-unreach ttl 61
49/udp    open|filtered tacacs          no-response
53/udp    closed        domain          port-unreach ttl 61
67/udp    open|filtered dhcps           no-response
68/udp    closed        dhcpc           port-unreach ttl 61
69/udp    open|filtered tftp            no-response
80/udp    closed        http            port-unreach ttl 61
88/udp    closed        kerberos-sec    port-unreach ttl 61
111/udp   closed        rpcbind         port-unreach ttl 61
120/udp   closed        cfdptkt         port-unreach ttl 61
123/udp   open|filtered ntp             no-response
135/udp   open|filtered msrpc           no-response
136/udp   closed        profile         port-unreach ttl 61
137/udp   closed        netbios-ns      port-unreach ttl 61
138/udp   closed        netbios-dgm     port-unreach ttl 61
139/udp   open|filtered netbios-ssn     no-response
158/udp   closed        pcmail-srv      port-unreach ttl 61
161/udp   closed        snmp            port-unreach ttl 61
162/udp   open|filtered snmptrap        no-response
177/udp   closed        xdmcp           port-unreach ttl 61
427/udp   closed        svrloc          port-unreach ttl 61
443/udp   closed        https           port-unreach ttl 61
445/udp   closed        microsoft-ds    port-unreach ttl 61
497/udp   open|filtered retrospect      no-response
500/udp   open|filtered isakmp          no-response
514/udp   open|filtered syslog          no-response
515/udp   closed        printer         port-unreach ttl 61
518/udp   open|filtered ntalk           no-response
520/udp   closed        route           port-unreach ttl 61
593/udp   closed        http-rpc-epmap  port-unreach ttl 61
623/udp   open|filtered asf-rmcp        no-response
626/udp   open|filtered serialnumberd   no-response
631/udp   closed        ipp             port-unreach ttl 61
996/udp   closed        vsinet          port-unreach ttl 61
997/udp   open|filtered maitrd          no-response
998/udp   open|filtered puparp          no-response
999/udp   open|filtered applix          no-response
1022/udp  open|filtered exp2            no-response
1023/udp  open|filtered unknown         no-response
1025/udp  closed        blackjack       port-unreach ttl 61
1026/udp  open|filtered win-rpc         no-response
1027/udp  open|filtered unknown         no-response
1028/udp  closed        ms-lsa          port-unreach ttl 61
1029/udp  open|filtered solid-mux       no-response
1030/udp  open|filtered iad1            no-response
1433/udp  closed        ms-sql-s        port-unreach ttl 61
1434/udp  closed        ms-sql-m        port-unreach ttl 61
1645/udp  closed        radius          port-unreach ttl 61
1646/udp  open|filtered radacct         no-response
1701/udp  closed        L2TP            port-unreach ttl 61
1718/udp  closed        h225gatedisc    port-unreach ttl 61
1719/udp  closed        h323gatestat    port-unreach ttl 61
1812/udp  open|filtered radius          no-response
1813/udp  open|filtered radacct         no-response
1900/udp  closed        upnp            port-unreach ttl 61
2000/udp  open|filtered cisco-sccp      no-response
2048/udp  open|filtered dls-monitor     no-response
2049/udp  open|filtered nfs             no-response
2222/udp  open|filtered msantipiracy    no-response
2223/udp  closed        rockwell-csp2   port-unreach ttl 61
3283/udp  closed        netassistant    port-unreach ttl 61
3456/udp  closed        IISrpc-or-vat   port-unreach ttl 61
3703/udp  closed        adobeserver-3   port-unreach ttl 61
4444/udp  closed        krb524          port-unreach ttl 61
4500/udp  closed        nat-t-ike       port-unreach ttl 61
5000/udp  closed        upnp            port-unreach ttl 61
5060/udp  closed        sip             port-unreach ttl 61
5353/udp  closed        zeroconf        port-unreach ttl 61
5632/udp  closed        pcanywherestat  port-unreach ttl 61
9200/udp  closed        wap-wsp         port-unreach ttl 61
10000/udp open|filtered ndmp            no-response
17185/udp closed        wdbrpc          port-unreach ttl 61
20031/udp open|filtered bakbonenetvault no-response
30718/udp closed        unknown         port-unreach ttl 61
31337/udp closed        BackOrifice     port-unreach ttl 61
32768/udp open|filtered omad            no-response
32769/udp open|filtered filenet-rpc     no-response
32771/udp closed        sometimes-rpc6  port-unreach ttl 61
32815/udp closed        unknown         port-unreach ttl 61
33281/udp open|filtered unknown         no-response
49152/udp open|filtered unknown         no-response
49153/udp closed        unknown         port-unreach ttl 61
49154/udp open|filtered unknown         no-response
49156/udp closed        unknown         port-unreach ttl 61
49181/udp closed        unknown         port-unreach ttl 61
49182/udp open|filtered unknown         no-response
49185/udp closed        unknown         port-unreach ttl 61
49186/udp open|filtered unknown         no-response
49188/udp open|filtered unknown         no-response
49190/udp open|filtered unknown         no-response
49191/udp open|filtered unknown         no-response
49192/udp closed        unknown         port-unreach ttl 61
49193/udp closed        unknown         port-unreach ttl 61
49194/udp closed        unknown         port-unreach ttl 61
49200/udp open|filtered unknown         no-response
49201/udp closed        unknown         port-unreach ttl 61
65024/udp closed        unknown         port-unreach ttl 61
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.18
OS details: Linux 2.6.18, Linux 2.6.30
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=10/21%OT=%CT=%CU=7%PV=Y%DS=5%DC=T%G=N%TM=6716B3C6%P
OS:=x86_64-pc-linux-gnu)SEQ()T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
OS:U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=19CF%RUD=G)IE(R=
OS:Y%DFI=N%T=40%CD=S)

Network Distance: 5 hops

TRACEROUTE (using port 4500/udp)
HOP RTT      ADDRESS
1   55.96 ms ATTACKER
2   55.95 ms ATTACKER
3   56.53 ms TARGET
4   ...
5   57.85 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Oct 21 16:04:22 2024 -- 1 IP address (1 host up) scanned in 307.28 seconds


```

#### Regular NMAP
```bash
# Nmap 7.94SVN scan initiated Mon Oct 21 16:06:25 2024 as: nmap -p- -sV -sC -vvv --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.057s latency).
Scanned at 2024-10-21 16:06:25 EDT for 40s
Not shown: 64704 closed tcp ports (reset), 828 filtered tcp ports (no-response)
Some closed ports may be reported as filtered due to --defeat-rst-ratelimit
PORT     STATE SERVICE REASON         VERSION
22/tcp   open  ssh     syn-ack ttl 61 OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
| ssh-hostkey: 
|   3072 c9:c3:da:15:28:3b:f1:f8:9a:36:df:4d:36:6b:a7:44 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDNEbgprJqVJa8R95Wkbo3cemB4fdRzos+v750LtPEnRs+IJQn5jcg5l89Tx4junU+AXzLflrMVo55gbuKeNTDtFRU9ltlIu4AU+f7lRlUlvAHlNjUbU/z3WBZ5ZU9j7Xc9WKjh1Ov7chC0UnDdyr5EGrIwlLzgk8zrWx364+S4JqLtER2/n0rhVxa9RCw0tR/oL24kMep4q7rFK6dThiRtQ9nsJFhh6yw8Fmdg7r4uohqH70UJurVwVNwFqtr/86e4VSSoITlMQPZrZFVvoSsjyL8LEODt1qznoLWudMD95Eo1YFSPID5VcS0kSElfYigjSr+9bNSdlzAof1mU6xJA67BggGNu6qITWWIJySXcropehnDAt2nv4zaKAUKc/T0ij9wkIBskuXfN88cEmZbu+gObKbLgwQSRQJIpQ+B/mA8CD4AiaTmEwGSWz1dVPp5Fgb6YVy6E4oO9ASuD9Q1JWuRmnn8uiHF/nPLs2LC2+rh3nPLXlV+MG/zUfQCrdrE=
|   256 26:03:2b:f6:da:90:1d:1b:ec:8d:8f:8d:1e:7e:3d:6b (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBCUhhvrIBs53SApXKZYHWBlpH50KO3POt8Y+WvTvHZ5YgRagAEU5eSnGkrnziCUvDWNShFhLHI7kQv+mx+4R6Wk=
|   256 fb:43:b2:b0:19:2f:d3:f6:bc:aa:60:67:ab:c1:af:37 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIN4MSEXnpONsc0ANUT6rFQPWsoVmRW4hrpSRq++xySM9
80/tcp   open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
|_http-title: Lugx Gaming Shop HTML5 Template
| http-methods: 
|_  Supported Methods: OPTIONS HEAD GET POST
|_http-server-header: Apache/2.4.56 (Debian)
8089/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
|_http-server-header: Apache/2.4.56 (Debian)
|_http-title: FlatPress
|_http-favicon: Unknown favicon MD5: 315957B26C1BD8805590E36985990754
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-generator: FlatPress fp-1.2.1
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Oct 21 16:07:05 2024 -- 1 IP address (1 host up) scanned in 40.24 seconds

```

