
## NMAP

```
# Nmap 7.94SVN scan initiated Sat Jul 27 19:19:39 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-07-27 19:19:40 EDT for 40s

PORT    STATE SERVICE     REASON          VERSION
139/tcp open  netbios-ssn syn-ack ttl 125 Microsoft Windows netbios-ssn
|_smb-enum-services: ERROR: Script execution failed (use -d to debug)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_smb-protocols: No dialects accepted. Something may be blocking the responses
|_smb-vuln-ms10-061: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb2-security-mode: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb-print-text: false
|_smb2-time: ERROR: Script execution failed (use -d to debug)
|_smb-mbenum: ERROR: Script execution failed (use -d to debug)
|_smb2-capabilities: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Jul 27 19:20:20 2024 -- 1 IP address (1 host up) scanned in 40.78 seconds

```
## enum4linux 

```
ENUM4LINUX - next generation (v1.3.3)

 ==========================
|    Target Information    |
 ==========================
[*] Target ........... TARGET
[*] Username ......... ''
[*] Random Username .. 'iupzzzcm'
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
[+] Long domain name is: vault.offsec

 ==============================================================
|    NetBIOS Names and Workgroup/Domain for TARGET    |
 ==============================================================
[V] Trying to get NetBIOS names information, running command: nmblookup -s /tmp/tmpb1rr45c7 -A TARGET
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
NetBIOS computer name: DC
NetBIOS domain name: VAULT
DNS domain: vault.offsec
FQDN: DC.vault.offsec
Derived membership: domain member
Derived domain: VAULT

 ============================================
|    RPC Session Check on TARGET    |
 ============================================
[*] Check for null session
[V] Attempting to make session, running command: smbclient -W VAULT -U % -s /tmp/tmpb1rr45c7 -t 5 -c help '//TARGET/ipc$'
[-] Could not establish null session: STATUS_ACCESS_DENIED
[*] Check for random user
[V] Attempting to make session, running command: smbclient -W VAULT -U iupzzzcm% -s /tmp/tmpb1rr45c7 -t 5 -c help '//TARGET/ipc$'
[+] Server allows session using username 'iupzzzcm', password ''
[H] Rerunning enumeration with user 'iupzzzcm' might give more results

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

[!] Aborting remainder of tests, sessions are possible, but not with the provided credentials (see session check results)

Completed after 7.58 seconds


```

## nbtscan 

```
Doing NBT name scan for addresses from TARGET



```

## smbclient 

```
do_connect: Connection to TARGET failed (Error NT_STATUS_RESOURCE_NAME_NOT_FOUND)

	Sharename       Type      Comment
	---------       ----      -------
	ADMIN$          Disk      Remote Admin
	C$              Disk      Default share
	DocumentsShare  Disk
	IPC$            IPC       Remote IPC
	NETLOGON        Disk      Logon server share
	SYSVOL          Disk      Logon server share
Reconnecting with SMB1 for workgroup listing.
Unable to connect with SMB1 -- no workgroup available


```

![Pasted image 20240727194135.png](Evidence/Pasted%20image%2020240727194135.png)

![Pasted image 20240727195722.png](Evidence/Pasted%20image%2020240727195722.png)

![Pasted image 20240727195733.png](Evidence/Pasted%20image%2020240727195733.png)

![Pasted image 20240727195933.png](Evidence/Pasted%20image%2020240727195933.png)

```
hashcat -m 5600 anirudh.hash  /usr/share/wordlists/rockyou.txt
```

![Pasted image 20240727200158.png](Evidence/Pasted%20image%2020240727200158.png)

password = SecureHM

![Pasted image 20240727200447.png](Evidence/Pasted%20image%2020240727200447.png)

Priv Esc
