
## NMAP

```
# Nmap 7.94SVN scan initiated Wed Jun 19 19:05:52 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.063s latency).
Scanned at 2024-06-19 19:05:54 EDT for 41s

PORT    STATE SERVICE     REASON          VERSION
139/tcp open  netbios-ssn syn-ack ttl 125 Microsoft Windows netbios-ssn
|_smb-enum-services: ERROR: Script execution failed (use -d to debug)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_smb2-security-mode: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb-vuln-ms10-061: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb2-time: ERROR: Script execution failed (use -d to debug)
|_smb2-capabilities: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb-print-text: false
|_smb-mbenum: ERROR: Script execution failed (use -d to debug)
|_smb-protocols: No dialects accepted. Something may be blocking the responses

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 19 19:06:35 2024 -- 1 IP address (1 host up) scanned in 43.32 seconds

```
## enum4linux 

```
Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Wed Jun 19 19:05:52 2024

 =========================================( Target Information )=========================================

Target ........... TARGET
RID Range ........ 500-550,1000-1050
Username ......... ''
Password ......... ''
Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none


 ==========================( Enumerating Workgroup/Domain on TARGET )==========================


[E] Can't find workgroup/domain



 ==============================( Nbtstat Information for TARGET )==============================

Looking up status of TARGET
No reply from TARGET

 ==================================( Session Check on TARGET )==================================


[E] Server doesn't allow session using username '', password ''.  Aborting remainder of tests.

```

## nbtscan 

```
Doing NBT name scan for addresses from TARGET



```

## smbclient 

```
session setup failed: NT_STATUS_ACCESS_DENIED


```

![Pasted image 20240619192636.png](Evidence/Pasted%20image%2020240619192636.png)

