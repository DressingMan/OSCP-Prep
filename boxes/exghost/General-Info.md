## Host Info
```
TARGET





```


## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Wed Oct  9 20:56:18 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.057s latency).
Scanned at 2024-10-09 20:56:18 EDT for 23s
Not shown: 997 filtered tcp ports (no-response)
PORT   STATE  SERVICE  REASON         VERSION
20/tcp closed ftp-data reset ttl 61
21/tcp open   ftp      syn-ack ttl 61 vsftpd 3.0.3
80/tcp open   http     syn-ack ttl 61 Apache httpd 2.4.41
|_http-title: 403 Forbidden
| http-methods: 
|_  Supported Methods: OPTIONS HEAD GET POST
|_http-server-header: Apache/2.4.41 (Ubuntu)
Device type: general purpose|storage-misc|firewall|WAP
Running (JUST GUESSING): Linux 2.6.X|3.X|4.X|2.4.X (86%), Synology DiskStation Manager 5.X (85%), WatchGuard Fireware 11.X (85%)
OS CPE: cpe:/o:linux:linux_kernel:2.6.32 cpe:/o:linux:linux_kernel:3.10 cpe:/o:linux:linux_kernel:4.4 cpe:/o:linux:linux_kernel cpe:/a:synology:diskstation_manager:5.1 cpe:/o:watchguard:fireware:11.8 cpe:/o:linux:linux_kernel:2.4
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Linux 2.6.32 (86%), Linux 2.6.32 or 3.10 (86%), Linux 2.6.39 (86%), Linux 3.10 - 3.12 (86%), Linux 4.4 (86%), Synology DiskStation Manager 5.1 (85%), Linux 2.6.35 (85%), Linux 4.9 (85%), Linux 3.4 (85%), Linux 3.5 (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=10/9%OT=21%CT=20%CU=%PV=Y%DS=4%DC=T%G=N%TM=67072649%P=x86_64-pc-linux-gnu)
SEQ(SP=FF%GCD=1%ISR=10F%TI=Z%II=I%TS=A)
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

Uptime guess: 44.738 days (since Mon Aug 26 03:13:30 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=255 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: Host: 127.0.0.1; OS: Unix

TRACEROUTE (using port 20/tcp)
HOP RTT      ADDRESS
1   55.06 ms ATTACKER
2   55.04 ms ATTACKER
3   56.21 ms TARGET
4   56.27 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Oct  9 20:56:41 2024 -- 1 IP address (1 host up) scanned in 22.79 seconds

```

#### Full Scan
```bash

Nmap scan report for TARGET
Host is up, received user-set (0.057s latency).
Scanned at 2024-10-09 20:56:18 EDT for 108s
Not shown: 65532 filtered tcp ports (no-response)
PORT   STATE  SERVICE  REASON         VERSION
20/tcp closed ftp-data reset ttl 61
21/tcp open   ftp      syn-ack ttl 61 vsftpd 3.0.3
80/tcp open   http     syn-ack ttl 61 Apache httpd 2.4.41
|_http-server-header: Apache/2.4.41 (Ubuntu)
| http-methods: 
|_  Supported Methods: OPTIONS HEAD GET POST
|_http-title: 403 Forbidden
Device type: general purpose
Running (JUST GUESSING): Linux 2.6.X|3.X|4.X (85%)
OS CPE: cpe:/o:linux:linux_kernel:2.6.32 cpe:/o:linux:linux_kernel:3.10 cpe:/o:linux:linux_kernel:4.2
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Linux 2.6.32 (85%), Linux 2.6.32 or 3.10 (85%), Linux 3.5 (85%), Linux 4.2 (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=10/9%OT=21%CT=20%CU=%PV=Y%DS=4%DC=T%G=N%TM=6707269E%P=x86_64-pc-linux-gnu)
SEQ(SP=104%GCD=1%ISR=103%TI=Z%TS=A)
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

Uptime guess: 44.739 days (since Mon Aug 26 03:13:30 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=260 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: Host: 127.0.0.1; OS: Unix

TRACEROUTE (using port 20/tcp)
HOP RTT      ADDRESS
1   54.60 ms ATTACKER
2   54.63 ms ATTACKER
3   55.91 ms TARGET
4   55.95 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Oct  9 20:58:06 2024 -- 1 IP address (1 host up) scanned in 107.60 seconds

```

#### UDP scan
```bash


```

