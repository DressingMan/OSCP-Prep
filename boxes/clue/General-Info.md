## Host Info
```
TARGET

OS: Windows
```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Fri Jun 21 13:30:06 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-06-21 13:30:06 EDT for 62s
Not shown: 994 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
80/tcp open http Apache httpd 2.4.38
| http-methods:
|_http-title: 403 Forbidden
139/tcp open netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp open netbios-ssn Samba smbd 4.9.5-Debian (workgroup: WORKGROUP)
3000/tcp open http Thin httpd
| http-methods:
|_http-title: Cassandra Web
8021/tcp open freeswitch-event FreeSWITCH mod_event_socket
Service Info: Hosts: 127.0.0.1, CLUE; OS: Linux; CPE: cpe:/o:linux:linux_kernel
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Fri Jun 21 13:31:08 2024 -- 1 IP address (1 host up) scanned in 62.47 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Fri Jun 21 13:30:06 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.065s latency).
Scanned at 2024-06-21 13:30:06 EDT for 185s
Not shown: 65529 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
80/tcp open http Apache httpd 2.4.38
|_http-title: 403 Forbidden
139/tcp open netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp open netbios-ssn Samba smbd 4.9.5-Debian (workgroup: WORKGROUP)
3000/tcp open http Thin httpd
| http-methods:
|_http-title: Cassandra Web
8021/tcp open freeswitch-event FreeSWITCH mod_event_socket
Service Info: Hosts: 127.0.0.1, CLUE; OS: Linux; CPE: cpe:/o:linux:linux_kernel
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Fri Jun 21 13:33:11 2024 -- 1 IP address (1 host up) scanned in 185.56 seconds
```

#### UDP scan
```

```

