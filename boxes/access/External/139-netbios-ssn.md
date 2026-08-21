
## NMAP

```
# Nmap 7.94SVN scan initiated Sat Jul 27 21:38:38 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.054s latency).
Scanned at 2024-07-27 21:38:39 EDT for 39s
PORT      STATE SERVICE        VERSION
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
|_smb2-security-mode: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb2-time: ERROR: Script execution failed (use -d to debug)
# Nmap done at Sat Jul 27 21:39:18 2024 -- 1 IP address (1 host up) scanned in 40.39 seconds
```
## enum4linux 

```
ENUM4LINUX - next generation (v1.3.3)

 ==========================
|    Target Information    |
 ==========================
[*] Target ........... TARGET
[*] Username ......... ''
[*] Random Username .. 'btfrmewt'
[*] Password ......... ''
[*] Timeout .......... 5 second(s)

 ========================================
|    Listener Scan on TARGET    |
 ========================================
[*] Checking LDAP
[+] LDAP is accessible on 389/tcp
[*] Checking LDAPS
[+] LDAPS is accessible on 636/tcp
[*] Checking SMB
[+] SMB is accessible on 445/tcp
[*] Checking SMB over NetBIOS
[+] SMB over NetBIOS is accessible on 139/tcp

 =======================================================
|    Domain Information via LDAP for TARGET    |
 =======================================================
[*] Trying LDAP
[+] Appears to be root/parent DC
[+] Long domain name is: access.offsec

 ==============================================================
|    NetBIOS Names and Workgroup/Domain for TARGET    |
 ==============================================================
[V] Trying to get NetBIOS names information, running command: nmblookup -s /tmp/tmp4paxbb3i -A TARGET
[-] Could not get NetBIOS names information via 'nmblookup': timed out

 ============================================
|    SMB Dialect Check on TARGET    |
 ============================================
[*] Trying on 445/tcp
[+] Supported dialects and settings:
Supported dialects:
  SMB 1.0: false
  SMB 2.02: true
  SMB 2.1: true
  SMB 3.0: true
  SMB 3.1.1: true
Preferred dialect: SMB 3.0
SMB1 only: false
SMB signing required: true

 ==============================================================
|    Domain Information via SMB session for TARGET    |
 ==============================================================
[*] Enumerating via unauthenticated SMB session on 445/tcp
[+] Found domain information via SMB
NetBIOS computer name: SERVER
NetBIOS domain name: ACCESS
DNS domain: access.offsec
FQDN: SERVER.access.offsec
Derived membership: domain member
Derived domain: ACCESS

 ============================================
|    RPC Session Check on TARGET    |
 ============================================
[*] Check for null session
[V] Attempting to make session, running command: smbclient -W ACCESS -U % -s /tmp/tmp4paxbb3i -t 5 -c help '//TARGET/ipc$'
[-] Could not establish null session: STATUS_ACCESS_DENIED
[*] Check for random user
[V] Attempting to make session, running command: smbclient -W ACCESS -U btfrmewt% -s /tmp/tmp4paxbb3i -t 5 -c help '//TARGET/ipc$'
[-] Could not establish random user session: STATUS_LOGON_FAILURE
[-] Sessions failed, neither null nor user sessions were possible

 ==================================================
|    OS Information via RPC for TARGET    |
 ==================================================
[*] Enumerating via unauthenticated SMB session on 445/tcp
[+] Found OS information via SMB
[*] Enumerating via 'srvinfo'
[-] Skipping 'srvinfo' run, not possible with provided credentials
[+] After merging OS information we have the following result:
OS: Windows 10, Windows Server 2019, Windows Server 2016
OS version: '10.0'
OS release: '1809'
OS build: '17763'
Native OS: not supported
Native LAN manager: not supported
Platform id: null
Server type: null
Server type string: null

[!] Aborting remainder of tests since sessions failed, rerun with valid credentials

Completed after 7.43 seconds

```

## nbtscan 

```
Doing NBT name scan for addresses from TARGET

```

## smbclient 

```
session setup failed: NT_STATUS_ACCESS_DENIED

```

![Pasted image 20240727215910.png](Evidence/Pasted%20image%2020240727215910.png)
