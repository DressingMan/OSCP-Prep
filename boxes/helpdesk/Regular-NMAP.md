```
# Nmap 7.94SVN scan initiated Fri Jun 21 09:54:04 2024 as: nmap -p- -sV -sC --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up (0.066s latency).
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
# Nmap done at Fri Jun 21 09:57:09 2024 -- 1 IP address (1 host up) scanned in 184.41 seconds
```
