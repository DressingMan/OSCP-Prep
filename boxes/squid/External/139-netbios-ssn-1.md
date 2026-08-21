
## NMAP

```
# Nmap 7.94SVN scan initiated Wed Jul 24 18:01:46 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-07-24 18:01:46 EDT for 41s

PORT    STATE SERVICE     REASON          VERSION
139/tcp open  netbios-ssn syn-ack ttl 125 Microsoft Windows netbios-ssn
|_smb-enum-services: ERROR: Script execution failed (use -d to debug)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_smb-protocols: No dialects accepted. Something may be blocking the responses
|_smb-print-text: false
|_smb2-security-mode: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb2-time: ERROR: Script execution failed (use -d to debug)
|_smb-vuln-ms10-061: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb-mbenum: ERROR: Script execution failed (use -d to debug)
|_smb2-capabilities: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jul 24 18:02:27 2024 -- 1 IP address (1 host up) scanned in 40.67 seconds

```
## enum4linux 

```
ENUM4LINUX - next generation (v1.3.3)

 ==========================
|    Target Information    |
 ==========================
[*] Target ........... TARGET
[*] Username ......... ''
[*] Random Username .. 'xlkldube'
[*] Password ......... ''
[*] Timeout .......... 5 second(s)

 ========================================
|    Listener Scan on TARGET    |
 ========================================
[*] Checking LDAP
[-] Could not connect to LDAP on 389/tcp: timed out
[*] Checking LDAPS
[-] Could not connect to LDAPS on 636/tcp: timed out
[*] Checking SMB
[+] SMB is accessible on 445/tcp
[*] Checking SMB over NetBIOS
[+] SMB over NetBIOS is accessible on 139/tcp

 ==============================================================
|    NetBIOS Names and Workgroup/Domain for TARGET    |
 ==============================================================
[V] Trying to get NetBIOS names information, running command: nmblookup -s /tmp/tmpeodyh4kp -A TARGET
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
SMB signing required: false

 ==============================================================
|    Domain Information via SMB session for TARGET    |
 ==============================================================
[*] Enumerating via unauthenticated SMB session on 445/tcp
[+] Found domain information via SMB
NetBIOS computer name: SQUID
NetBIOS domain name: ''
DNS domain: SQUID
FQDN: SQUID
Derived membership: workgroup member
Derived domain: unknown

 ============================================
|    RPC Session Check on TARGET    |
 ============================================
[*] Check for null session
[V] Attempting to make session, running command: smbclient -W WORKGROUP -U % -s /tmp/tmpeodyh4kp -t 5 -c help '//TARGET/ipc$'
[-] Could not establish null session: STATUS_ACCESS_DENIED
[*] Check for random user
[V] Attempting to make session, running command: smbclient -W WORKGROUP -U xlkldube% -s /tmp/tmpeodyh4kp -t 5 -c help '//TARGET/ipc$'
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

Completed after 17.29 seconds


```

## nbtscan 

```
Doing NBT name scan for addresses from TARGET



```

## smbclient 

```
session setup failed: NT_STATUS_ACCESS_DENIED


```

