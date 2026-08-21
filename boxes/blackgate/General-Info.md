## Host Info
```
TARGET
```


## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Mon Jun 10 16:57:23 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.063s latency).
Scanned at 2024-06-10 16:57:24 EDT for 24s
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 61 OpenSSH 8.3p1 Ubuntu 1ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 37:21:14:3e:23:e5:13:40:20:05:f9:79:e0:82:0b:09 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDErzUX3Jeg2oRWhqelAA3/QrsFYoyDVaXbJK0ghZTX1i3mZY8SXopUZC09JD/6S+Ye+nFW2/6rnXHltIVWEALmPDrlDOV5m+LGujzXqc5YJcylNnwSjz9TjCHlPa+PrMdyp2NyT+Wt2w6jhVWA1sowq8R4ZDkqvpQwz9rUOVk5IRiV6fgdEuHBBXKQZu9S00iPNC5hhfmclk5k2dPtFqQRlosZfjDjv5E8Zo8YwLGonmWciNQQB8DWX47R08noPMseQMYR707ABcIgx4+DKMZ7/HlOzqwoqFdyvMSdPf5lz+cPG/aI0N6qua80uxbXg0rvMNQuZd73d5jA+Yp3eIkI4lHQqjXO4B0Gbl4lpcHTWCdUI93dLbBy13J0NdTG+vqkXszDBXr19rWaD+yeXg8FQt5ViHr7N/Pr77zFjOiAq4AjRNt6j8e+kX0Cqwov1RwUc4R1JPfmEIZqm8Ds/z+jDhkhLoJP4yjE8xNHhOz8lUk+bZh3zGuS3+97Mrkh3Rs=
|   256 b9:8d:bd:90:55:7c:84:cc:a0:7f:a8:b4:d3:55:06:a7 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBPed4/WiZ+RjcALVwQnLf74Byu1yb40zjCfDT+DBa4jiTzciU5Ql1fhEzanZGgt5VuK0y5ZAgG7f54yL9iVcaU8=
|   256 07:07:29:7a:4c:7c:f2:b0:1f:3c:3f:2b:a1:56:9e:0a (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIJLFhMCuSltbhF2Mj0Xz0A3ZSEhcu8LOF9hX8bqGirVH
Aggressive OS guesses: Linux 2.6.32 (87%), Linux 2.6.32 or 3.10 (87%), Linux 2.6.39 (87%), Linux 3.10 - 3.12 (87%), Linux 3.5 (87%), Linux 4.4 (87%), Synology DiskStation Manager 5.1 (87%), WatchGuard Fireware 11.8 (87%), Linux 2.6.35 (87%), Linux 4.9 (87%)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=6/10%OT=22%CT=1%CU=39105%PV=Y%DS=4%DC=T%G=Y%TM=6667
OS:68CC%P=x86_64-pc-linux-gnu)SEQ(SP=100%GCD=1%ISR=10C%TI=Z%TS=A)SEQ(SP=107
OS:%GCD=1%ISR=10A%TI=Z%TS=A)SEQ(SP=F9%GCD=1%ISR=10A%TI=Z%TS=A)OPS(O1=M551ST
OS:11NW7%O2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M5
OS:51ST11)WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)ECN(R=Y%DF=Y%
OS:T=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S+%F=AS%RD=0%Q=)
OS:T2(R=N)T3(R=N)T4(R=N)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=
OS:N)T7(R=N)U1(R=N)U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=
OS:606C%RUD=G)IE(R=N)IE(R=Y%DFI=N%T=40%CD=S)

Uptime guess: 13.720 days (since Mon May 27 23:40:25 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=256 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 23/tcp)
HOP RTT      ADDRESS
1   67.50 ms ATTACKER
2   67.34 ms ATTACKER
3   67.74 ms TARGET
4   68.88 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun 10 16:57:48 2024 -- 1 IP address (1 host up) scanned in 24.24 seconds

```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Mon Jun 10 16:57:24 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.070s latency).
Scanned at 2024-06-10 16:57:24 EDT for 133s
Not shown: 65533 closed tcp ports (reset)
PORT     STATE SERVICE REASON         VERSION
22/tcp   open  ssh     syn-ack ttl 61 OpenSSH 8.3p1 Ubuntu 1ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 37:21:14:3e:23:e5:13:40:20:05:f9:79:e0:82:0b:09 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDErzUX3Jeg2oRWhqelAA3/QrsFYoyDVaXbJK0ghZTX1i3mZY8SXopUZC09JD/6S+Ye+nFW2/6rnXHltIVWEALmPDrlDOV5m+LGujzXqc5YJcylNnwSjz9TjCHlPa+PrMdyp2NyT+Wt2w6jhVWA1sowq8R4ZDkqvpQwz9rUOVk5IRiV6fgdEuHBBXKQZu9S00iPNC5hhfmclk5k2dPtFqQRlosZfjDjv5E8Zo8YwLGonmWciNQQB8DWX47R08noPMseQMYR707ABcIgx4+DKMZ7/HlOzqwoqFdyvMSdPf5lz+cPG/aI0N6qua80uxbXg0rvMNQuZd73d5jA+Yp3eIkI4lHQqjXO4B0Gbl4lpcHTWCdUI93dLbBy13J0NdTG+vqkXszDBXr19rWaD+yeXg8FQt5ViHr7N/Pr77zFjOiAq4AjRNt6j8e+kX0Cqwov1RwUc4R1JPfmEIZqm8Ds/z+jDhkhLoJP4yjE8xNHhOz8lUk+bZh3zGuS3+97Mrkh3Rs=
|   256 b9:8d:bd:90:55:7c:84:cc:a0:7f:a8:b4:d3:55:06:a7 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBPed4/WiZ+RjcALVwQnLf74Byu1yb40zjCfDT+DBa4jiTzciU5Ql1fhEzanZGgt5VuK0y5ZAgG7f54yL9iVcaU8=
|   256 07:07:29:7a:4c:7c:f2:b0:1f:3c:3f:2b:a1:56:9e:0a (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIJLFhMCuSltbhF2Mj0Xz0A3ZSEhcu8LOF9hX8bqGirVH
6379/tcp open  redis   syn-ack ttl 61 Redis key-value store 4.0.14
Aggressive OS guesses: Linux 2.6.32 (88%), Linux 2.6.39 (88%), Linux 3.10 - 3.12 (88%), Linux 3.4 (88%), Linux 4.4 (88%), Synology DiskStation Manager 5.1 (88%), WatchGuard Fireware 11.8 (88%), Linux 2.6.35 (87%), Linux 3.10 (87%), Linux 2.6.32 or 3.10 (87%)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=6/10%OT=22%CT=1%CU=37370%PV=Y%DS=4%DC=T%G=Y%TM=6667
OS:6939%P=x86_64-pc-linux-gnu)SEQ(TI=Z%TS=A)SEQ(SP=105%GCD=1%ISR=10D%TI=Z%I
OS:I=I%TS=A)SEQ(SP=106%GCD=1%ISR=10C%TI=Z%TS=8)SEQ(SP=106%GCD=1%ISR=10D%TI=
OS:Z%II=I%TS=9)SEQ(SP=106%GCD=1%ISR=10D%TI=Z%II=I%TS=A)OPS(O1=M551ST11NW7%O
OS:2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)
OS:WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)ECN(R=N)ECN(R=Y%DF=Y
OS:%T=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)T1(R=N)T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS
OS:%RD=0%Q=)T1(R=Y%DF=Y%T=40%S=O%A=O%F=AS%RD=0%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S+
OS:%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(R=N)T5(R=N)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=O%F
OS:=AR%O=%RD=0%Q=)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=N)T7(R
OS:=N)U1(R=N)U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=7451%R
OS:UD=G)IE(R=N)IE(R=Y%DFI=N%T=40%CD=S)

Uptime guess: 13.722 days (since Mon May 27 23:40:25 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=261 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 5900/tcp)
HOP RTT       ADDRESS
1   156.42 ms ATTACKER
2   156.61 ms ATTACKER
3   156.62 ms TARGET
4   156.65 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun 10 16:59:37 2024 -- 1 IP address (1 host up) scanned in 133.50 seconds

```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Mon Jun 10 16:57:23 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/... -oX /home/kali/... TARGET
Warning: TARGET giving up on port because retransmission cap hit (6).
Increasing send delay for TARGET from 100 to 200 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for TARGET from 200 to 400 due to 11 out of 13 dropped probes since last increase.
Increasing send delay for TARGET from 400 to 800 due to 11 out of 11 dropped probes since last increase.
Nmap scan report for TARGET
Host is up, received user-set (0.075s latency).
Scanned at 2024-06-10 16:57:24 EDT for 222s
Not shown: 82 closed udp ports (port-unreach)
PORT      STATE         SERVICE      REASON      VERSION
49/udp    open|filtered tacacs       no-response
123/udp   open|filtered ntp          no-response
139/udp   open|filtered netbios-ssn  no-response
497/udp   open|filtered retrospect   no-response
514/udp   open|filtered syslog       no-response
520/udp   open|filtered route        no-response
623/udp   open|filtered asf-rmcp     no-response
631/udp   open|filtered ipp          no-response
997/udp   open|filtered maitrd       no-response
1026/udp  open|filtered win-rpc      no-response
1027/udp  open|filtered unknown      no-response
1645/udp  open|filtered radius       no-response
1718/udp  open|filtered h225gatedisc no-response
2048/udp  open|filtered dls-monitor  no-response
4500/udp  open|filtered nat-t-ike    no-response
5000/udp  open|filtered upnp         no-response
49192/udp open|filtered unknown      no-response
49200/udp open|filtered unknown      no-response
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.18
OS details: Linux 2.6.18, Linux 2.6.30
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=6/10%OT=%CT=%CU=7%PV=Y%DS=4%DC=T%G=N%TM=66676992%P=
OS:x86_64-pc-linux-gnu)SEQ(II=I)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%
OS:Q=)U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=142%RUD=G)IE(
OS:R=Y%DFI=N%T=40%CD=S)

Network Distance: 4 hops

TRACEROUTE (using port 32815/udp)
HOP RTT      ADDRESS
1   57.22 ms ATTACKER
2   57.20 ms ATTACKER
3   57.22 ms TARGET
4   57.26 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun 10 17:01:06 2024 -- 1 IP address (1 host up) scanned in 222.66 seconds

```

