
## NMAP

```
# Nmap 7.94SVN scan initiated Mon Jul 15 15:25:30 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-07-15 15:25:32 EDT for 40s
PORT      STATE SERVICE        VERSION
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
|_smb2-time: ERROR: Script execution failed (use -d to debug)
|_smb2-security-mode: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
# Nmap done at Mon Jul 15 15:26:12 2024 -- 1 IP address (1 host up) scanned in 43.11 seconds
```
## enum4linux 

```
ENUM4LINUX - next generation (v1.3.3)

 ==========================
|    Target Information    |
 ==========================
[*] Target ........... TARGET
[*] Username ......... ''
[*] Random Username .. 'hmahbyqs'
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
[+] Long domain name is: hutch.offsec

 ==============================================================
|    NetBIOS Names and Workgroup/Domain for TARGET    |
 ==============================================================
[V] Trying to get NetBIOS names information, running command: nmblookup -s /tmp/tmpxlsh5ocf -A TARGET
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
NetBIOS computer name: HUTCHDC
NetBIOS domain name: HUTCH
DNS domain: hutch.offsec
FQDN: hutchdc.hutch.offsec
Derived membership: domain member
Derived domain: HUTCH

 ============================================
|    RPC Session Check on TARGET    |
 ============================================
[*] Check for null session
[V] Attempting to make session, running command: smbclient -W HUTCH -U % -s /tmp/tmpxlsh5ocf -t 5 -c help '//TARGET/ipc$'
[+] Server allows session using username '', password ''
[*] Check for random user
[V] Attempting to make session, running command: smbclient -W HUTCH -U hmahbyqs% -s /tmp/tmpxlsh5ocf -t 5 -c help '//TARGET/ipc$'
[-] Could not establish random user session: STATUS_LOGON_FAILURE

 ======================================================
|    Domain Information via RPC for TARGET    |
 ======================================================
[V] Attempting to get domain SID, running command: rpcclient -W HUTCH -U % -s /tmp/tmpxlsh5ocf -c lsaquery TARGET
[+] Domain: HUTCH
[+] Domain SID: S-1-5-21-2216925765-458455009-2806096489
[+] Membership: domain member

 ==================================================
|    OS Information via RPC for TARGET    |
 ==================================================
[*] Enumerating via unauthenticated SMB session on 445/tcp
[+] Found OS information via SMB
[*] Enumerating via 'srvinfo'
[V] Attempting to get OS info with command, running command: rpcclient -W HUTCH -U % -s /tmp/tmpxlsh5ocf -c srvinfo TARGET
[-] Could not get OS info via 'srvinfo': STATUS_ACCESS_DENIED
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

 ========================================
|    Users via RPC on TARGET    |
 ========================================
[*] Enumerating users via 'querydispinfo'
[V] Attempting to get userlist, running command: rpcclient -W HUTCH -U % -s /tmp/tmpxlsh5ocf -c querydispinfo TARGET
[-] Could not find users via 'querydispinfo': STATUS_ACCESS_DENIED
[*] Enumerating users via 'enumdomusers'
[V] Attempting to get userlist, running command: rpcclient -W HUTCH -U % -s /tmp/tmpxlsh5ocf -c enumdomusers TARGET
[-] Could not find users via 'enumdomusers': STATUS_ACCESS_DENIED

 =========================================
|    Groups via RPC on TARGET    |
 =========================================
[*] Enumerating local groups
[V] Attempting to get local groups, running command: rpcclient -W HUTCH -U % -s /tmp/tmpxlsh5ocf -c 'enumalsgroups domain' TARGET
[-] Could not get groups via 'enumalsgroups domain': STATUS_ACCESS_DENIED
[*] Enumerating builtin groups
[V] Attempting to get builtin groups, running command: rpcclient -W HUTCH -U % -s /tmp/tmpxlsh5ocf -c 'enumalsgroups builtin' TARGET
[-] Could not get groups via 'enumalsgroups builtin': STATUS_ACCESS_DENIED
[*] Enumerating domain groups
[V] Attempting to get domain groups, running command: rpcclient -W HUTCH -U % -s /tmp/tmpxlsh5ocf -c enumdomgroups TARGET
[-] Could not get groups via 'enumdomgroups': STATUS_ACCESS_DENIED

 =========================================
|    Shares via RPC on TARGET    |
 =========================================
[V] Attempting to get share list using authentication, running command: smbclient -W HUTCH -U % -s /tmp/tmpxlsh5ocf -t 5 -L //TARGET -g
[*] Enumerating shares
[+] Found 0 share(s) for user '' with password '', try a different user

 ============================================
|    Policies via RPC for TARGET    |
 ============================================
[*] Trying port 445/tcp
[-] SMB connection error on port 445/tcp: STATUS_ACCESS_DENIED
[*] Trying port 139/tcp
[-] SMB connection error on port 139/tcp: session failed

 ============================================
|    Printers via RPC for TARGET    |
 ============================================
[V] Attempting to get printer info, running command: rpcclient -W HUTCH -U % -s /tmp/tmpxlsh5ocf -c enumprinters TARGET
[-] Could not get printer info via 'enumprinters': STATUS_ACCESS_DENIED

Completed after 15.60 seconds

```

## nbtscan 

```
Doing NBT name scan for addresses from TARGET

```

## smbclient 

```
do_connect: Connection to TARGET failed (Error NT_STATUS_RESOURCE_NAME_NOT_FOUND)
Anonymous login successful

	Sharename       Type      Comment
	---------       ----      -------
Reconnecting with SMB1 for workgroup listing.
Unable to connect with SMB1 -- no workgroup available

```

![Pasted image 20240715172933.png](Evidence/Pasted%20image%2020240715172933.png)

