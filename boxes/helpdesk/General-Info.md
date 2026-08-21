## Host Info
```
CVE-2011-0966
CVE-2017-0143
CVE-2003-0104
CVE-2001-0926

TARGET

OS: Windows
```

## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Fri Jun 21 09:53:37 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.065s latency).
Scanned at 2024-06-21 09:53:37 EDT for 68s
Not shown: 995 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
445/tcp open microsoft-ds Windows Server (R) 2008 Standard 6001 Service Pack 1 microsoft-ds (work...
3389/tcp open ms-wbt-server Microsoft Terminal Service
8080/tcp open http Apache Tomcat/Coyote JSP engine 1.1
| http-methods:
|_http-title: ManageEngine ServiceDesk Plus
Service Info: Host: HELPDESK; OS: Windows; CPE: cpe:/o:microsoft:windows, cpe:/o:microsoft:windows_server_2008:r2
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Fri Jun 21 09:54:45 2024 -- 1 IP address (1 host up) scanned in 68.75 seconds
```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Fri Jun 21 09:53:37 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-06-21 09:53:37 EDT for 148s
Not shown: 65530 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
445/tcp open microsoft-ds Windows Server (R) 2008 Standard 6001 Service Pack 1 microsoft-ds (work...
3389/tcp open ms-wbt-server Microsoft Terminal Service
8080/tcp open http Apache Tomcat/Coyote JSP engine 1.1
|_http-title: ManageEngine ServiceDesk Plus
Service Info: Host: HELPDESK; OS: Windows; CPE: cpe:/o:microsoft:windows, cpe:/o:microsoft:windows_server_2008:r2
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Fri Jun 21 09:56:05 2024 -- 1 IP address (1 host up) scanned in 148.46 seconds
```

#### UDP scan
```

```

