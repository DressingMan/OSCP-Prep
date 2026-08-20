## Host Info
```
TARGET




```


## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Thu Oct 24 16:31:20 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -703070 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -703070 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-10-24 16:31:20 EDT for 18s
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
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-title: htmLawed (1.2.5) test
|_http-server-header: Apache/2.4.56 (Debian)
Device type: general purpose|storage-misc|firewall
Running (JUST GUESSING): Linux 2.6.X|3.X|4.X (85%), Synology DiskStation Manager 5.X (85%), WatchGuard Fireware 11.X (85%)
OS CPE: cpe:/o:linux:linux_kernel:2.6.32 cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:4.4 cpe:/o:linux:linux_kernel cpe:/a:synology:diskstation_manager:5.1 cpe:/o:watchguard:fireware:11.8
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Linux 2.6.32 (85%), Linux 2.6.39 (85%), Linux 3.10 - 3.12 (85%), Linux 3.4 (85%), Linux 4.4 (85%), Synology DiskStation Manager 5.1 (85%), WatchGuard Fireware 11.8 (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=10/24%OT=22%CT=1%CU=%PV=Y%DS=4%DC=T%G=N%TM=671AAEAA%P=x86_64-pc-linux-gnu)
SEQ(SP=106%GCD=1%ISR=10D%TI=Z%TS=A)
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

Uptime guess: 15.287 days (since Wed Oct  9 09:39:04 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=262 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 995/tcp)
HOP RTT      ADDRESS
1   56.70 ms ATTACKER
2   56.68 ms ATTACKER
3   57.77 ms TARGET
4   57.77 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Thu Oct 24 16:31:38 2024 -- 1 IP address (1 host up) scanned in 18.92 seconds

```

#### Full Scan
```bash

# Nmap 7.94SVN scan initiated Thu Oct 24 16:31:20 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -204313 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -204313 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -200237 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -200237 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -204041 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -204041 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -174720 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -174720 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -248541 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -248541 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -173552 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -173552 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -243133 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -243133 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -459472 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -459472 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.055s latency).
Scanned at 2024-10-24 16:31:20 EDT for 76s
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
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache/2.4.56 (Debian)
|_http-title: htmLawed (1.2.5) test
Aggressive OS guesses: Linux 2.6.32 (87%), Linux 3.4 (87%), Linux 3.5 (87%), Linux 4.2 (87%), Linux 4.4 (87%), Synology DiskStation Manager 5.1 (87%), Linux 2.6.35 (87%), Linux 3.10 (87%), Linux 2.6.32 or 3.10 (86%), Linux 2.6.39 (86%)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=10/24%OT=22%CT=1%CU=41391%PV=Y%DS=4%DC=T%G=Y%TM=671
OS:AAEE4%P=x86_64-pc-linux-gnu)SEQ(SP=107%GCD=1%ISR=109%TI=Z%TS=A)OPS(O1=M5
OS:51ST11NW7%O2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O
OS:6=M551ST11)WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)ECN(R=Y%D
OS:F=Y%T=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S+%F=AS%RD=0
OS:%Q=)T2(R=N)T3(R=N)T4(R=N)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T
OS:6(R=N)T7(R=N)U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=959
OS:B%RUD=G)IE(R=Y%DFI=N%T=40%CD=S)

Uptime guess: 15.287 days (since Wed Oct  9 09:39:04 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=263 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 3306/tcp)
HOP RTT      ADDRESS
1   57.45 ms ATTACKER
2   57.44 ms ATTACKER
3   58.55 ms TARGET
4   58.57 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Thu Oct 24 16:32:36 2024 -- 1 IP address (1 host up) scanned in 76.85 seconds

```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Thu Oct 24 16:33:34 2024 as: nmap -vvv --top-ports 100 -sU -oN nmap_udp TARGET
Increasing send delay for TARGET from 800 to 1000 due to 11 out of 16 dropped probes since last increase.
Nmap scan report for TARGET
Host is up, received reset ttl 61 (0.054s latency).
Scanned at 2024-10-24 16:33:34 EDT for 137s

PORT      STATE  SERVICE         REASON
7/udp     closed echo            port-unreach ttl 61
9/udp     closed discard         port-unreach ttl 61
17/udp    closed qotd            port-unreach ttl 61
19/udp    closed chargen         port-unreach ttl 61
49/udp    closed tacacs          port-unreach ttl 61
53/udp    closed domain          port-unreach ttl 61
67/udp    closed dhcps           port-unreach ttl 61
68/udp    closed dhcpc           port-unreach ttl 61
69/udp    closed tftp            port-unreach ttl 61
80/udp    closed http            port-unreach ttl 61
88/udp    closed kerberos-sec    port-unreach ttl 61
111/udp   closed rpcbind         port-unreach ttl 61
120/udp   closed cfdptkt         port-unreach ttl 61
123/udp   closed ntp             port-unreach ttl 61
135/udp   closed msrpc           port-unreach ttl 61
136/udp   closed profile         port-unreach ttl 61
137/udp   closed netbios-ns      port-unreach ttl 61
138/udp   closed netbios-dgm     port-unreach ttl 61
139/udp   closed netbios-ssn     port-unreach ttl 61
158/udp   closed pcmail-srv      port-unreach ttl 61
161/udp   closed snmp            port-unreach ttl 61
162/udp   closed snmptrap        port-unreach ttl 61
177/udp   closed xdmcp           port-unreach ttl 61
427/udp   closed svrloc          port-unreach ttl 61
443/udp   closed https           port-unreach ttl 61
445/udp   closed microsoft-ds    port-unreach ttl 61
497/udp   closed retrospect      port-unreach ttl 61
500/udp   closed isakmp          port-unreach ttl 61
514/udp   closed syslog          port-unreach ttl 61
515/udp   closed printer         port-unreach ttl 61
518/udp   closed ntalk           port-unreach ttl 61
520/udp   closed route           port-unreach ttl 61
593/udp   closed http-rpc-epmap  port-unreach ttl 61
623/udp   closed asf-rmcp        port-unreach ttl 61
626/udp   closed serialnumberd   port-unreach ttl 61
631/udp   closed ipp             port-unreach ttl 61
996/udp   closed vsinet          port-unreach ttl 61
997/udp   closed maitrd          port-unreach ttl 61
998/udp   closed puparp          port-unreach ttl 61
999/udp   closed applix          port-unreach ttl 61
1022/udp  closed exp2            port-unreach ttl 61
1023/udp  closed unknown         port-unreach ttl 61
1025/udp  closed blackjack       port-unreach ttl 61
1026/udp  closed win-rpc         port-unreach ttl 61
1027/udp  closed unknown         port-unreach ttl 61
1028/udp  closed ms-lsa          port-unreach ttl 61
1029/udp  closed solid-mux       port-unreach ttl 61
1030/udp  closed iad1            port-unreach ttl 61
1433/udp  closed ms-sql-s        port-unreach ttl 61
1434/udp  closed ms-sql-m        port-unreach ttl 61
1645/udp  closed radius          port-unreach ttl 61
1646/udp  closed radacct         port-unreach ttl 61
1701/udp  closed L2TP            port-unreach ttl 61
1718/udp  closed h225gatedisc    port-unreach ttl 61
1719/udp  closed h323gatestat    port-unreach ttl 61
1812/udp  closed radius          port-unreach ttl 61
1813/udp  closed radacct         port-unreach ttl 61
1900/udp  closed upnp            port-unreach ttl 61
2000/udp  closed cisco-sccp      port-unreach ttl 61
2048/udp  closed dls-monitor     port-unreach ttl 61
2049/udp  closed nfs             port-unreach ttl 61
2222/udp  closed msantipiracy    port-unreach ttl 61
2223/udp  closed rockwell-csp2   port-unreach ttl 61
3283/udp  closed netassistant    port-unreach ttl 61
3456/udp  closed IISrpc-or-vat   port-unreach ttl 61
3703/udp  closed adobeserver-3   port-unreach ttl 61
4444/udp  closed krb524          port-unreach ttl 61
4500/udp  closed nat-t-ike       port-unreach ttl 61
5000/udp  closed upnp            port-unreach ttl 61
5060/udp  closed sip             port-unreach ttl 61
5353/udp  closed zeroconf        port-unreach ttl 61
5632/udp  closed pcanywherestat  port-unreach ttl 61
9200/udp  closed wap-wsp         port-unreach ttl 61
10000/udp closed ndmp            port-unreach ttl 61
17185/udp closed wdbrpc          port-unreach ttl 61
20031/udp closed bakbonenetvault port-unreach ttl 61
30718/udp closed unknown         port-unreach ttl 61
31337/udp closed BackOrifice     port-unreach ttl 61
32768/udp closed omad            port-unreach ttl 61
32769/udp closed filenet-rpc     port-unreach ttl 61
32771/udp closed sometimes-rpc6  port-unreach ttl 61
32815/udp closed unknown         port-unreach ttl 61
33281/udp closed unknown         port-unreach ttl 61
49152/udp closed unknown         port-unreach ttl 61
49153/udp closed unknown         port-unreach ttl 61
49154/udp closed unknown         port-unreach ttl 61
49156/udp closed unknown         port-unreach ttl 61
49181/udp closed unknown         port-unreach ttl 61
49182/udp closed unknown         port-unreach ttl 61
49185/udp closed unknown         port-unreach ttl 61
49186/udp closed unknown         port-unreach ttl 61
49188/udp closed unknown         port-unreach ttl 61
49190/udp closed unknown         port-unreach ttl 61
49191/udp closed unknown         port-unreach ttl 61
49192/udp closed unknown         port-unreach ttl 61
49193/udp closed unknown         port-unreach ttl 61
49194/udp closed unknown         port-unreach ttl 61
49200/udp closed unknown         port-unreach ttl 61
49201/udp closed unknown         port-unreach ttl 61
65024/udp closed unknown         port-unreach ttl 61

Read data files from: /usr/bin/../share/nmap
# Nmap done at Thu Oct 24 16:35:51 2024 -- 1 IP address (1 host up) scanned in 136.92 seconds


```

#### Regular NMAP
```bash
# Nmap 7.94SVN scan initiated Thu Oct 24 16:31:23 2024 as: nmap -p- -sV -sC -vvv --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.061s latency).
Scanned at 2024-10-24 16:31:23 EDT for 35s
Not shown: 65371 closed tcp ports (reset), 162 filtered tcp ports (no-response)
Some closed ports may be reported as filtered due to --defeat-rst-ratelimit
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
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-title: htmLawed (1.2.5) test
|_http-server-header: Apache/2.4.56 (Debian)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Thu Oct 24 16:31:58 2024 -- 1 IP address (1 host up) scanned in 34.78 seconds

```

