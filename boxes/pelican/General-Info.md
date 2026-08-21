## Host Info
```

 TARGET

```

## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Thu Oct 17 16:41:45 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-10-17 16:41:45 EDT for 39s
Not shown: 993 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
139/tcp open netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp open netbios-ssn Samba smbd 4.9.5-Debian (workgroup: WORKGROUP)
631/tcp open ipp CUPS 2.2
|_http-title: Forbidden - CUPS v2.2.10
| http-methods:
|_  Potentially risky methods: PUT
2222/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
8080/tcp open http Jetty 1.0
|_http-title: Error 404 Not Found
8081/tcp open http nginx 1.14.2
| http-methods:
|_http-title: Did not follow redirect to http://TARGET:8080/exhibitor/v1/ui/index.html
Service Info: Host: PELICAN; OS: Linux; CPE: cpe:/o:linux:linux_kernel
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Thu Oct 17 16:42:24 2024 -- 1 IP address (1 host up) scanned in 39.22 seconds
```

#### Full Scan
```bash
# Nmap 7.94SVN scan initiated Thu Oct 17 16:41:45 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-10-17 16:41:45 EDT for 81s
Not shown: 65526 closed tcp ports (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
139/tcp open netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp open netbios-ssn Samba smbd 4.9.5-Debian (workgroup: WORKGROUP)
631/tcp open ssl/ipp CUPS 2.2
| ssl-cert: Subject: commonName=pelican/organizationName=pelican/stateOrProvinceName=Unknown/countryName=US...
| http-methods:
|_  Potentially risky methods: PUT
|_http-title: Forbidden - CUPS v2.2.10
2181/tcp open zookeeper Zookeeper 3.4.6-1569965 (Built on 02/20/2014)
2222/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
8080/tcp open http Jetty 1.0
|_http-title: Error 404 Not Found
8081/tcp open http nginx 1.14.2
|_http-title: Did not follow redirect to http://TARGET:8080/exhibitor/v1/ui/index.html
44267/tcp open java-rmi Java RMI
Service Info: Host: PELICAN; OS: Linux; CPE: cpe:/o:linux:linux_kernel
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Thu Oct 17 16:43:06 2024 -- 1 IP address (1 host up) scanned in 81.13 seconds
```

#### UDP scan
```bash

```

#### Regular NMAP TCP
```bash
# Nmap 7.94SVN scan initiated Thu Oct 17 16:53:08 2024 as: nmap -p- -sV -sC -vvv --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up, received reset ttl 61 (0.062s latency).
Scanned at 2024-10-17 16:53:08 EDT for 48s
Not shown: 65132 closed tcp ports (reset), 394 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
139/tcp open netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp open netbios-ssn Samba smbd 4.9.5-Debian (workgroup: WORKGROUP)
631/tcp open ipp CUPS 2.2
|_http-title: Forbidden - CUPS v2.2.10
| http-methods:
|_  Potentially risky methods: PUT
2181/tcp open zookeeper Zookeeper 3.4.6-1569965 (Built on 02/20/2014)
2222/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
8080/tcp open http Jetty 1.0
|_http-title: Error 404 Not Found
8081/tcp open http nginx 1.14.2
| http-methods:
|_http-title: Did not follow redirect to http://TARGET:8080/exhibitor/v1/ui/index.html
44267/tcp open java-rmi Java RMI
Service Info: Host: PELICAN; OS: Linux; CPE: cpe:/o:linux:linux_kernel
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Thu Oct 17 16:53:56 2024 -- 1 IP address (1 host up) scanned in 48.73 seconds
```

