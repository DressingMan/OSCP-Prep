
```bash
# Nmap 7.94SVN scan initiated Thu Oct 17 16:43:06 2024 as: nmap -vv --reason -Pn -T4 -sV -p 44267 --script=banner,rmi-vuln-classloader,rmi-dumpregistry -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.055s latency).
Scanned at 2024-10-17 16:43:06 EDT for 25s

PORT      STATE SERVICE  REASON         VERSION
44267/tcp open  java-rmi syn-ack ttl 61 Java RMI
| rmi-vuln-classloader: 
|   VULNERABLE:
|   RMI registry default configuration remote code execution vulnerability
|     State: VULNERABLE
|       Default configuration of RMI registry allows loading classes from remote URLs which can lead to remote code execution.
|       
|     References:
|_      https://github.com/rapid7/metasploit-framework/blob/master/modules/exploits/multi/misc/java_rmi_server.rb

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Thu Oct 17 16:43:31 2024 -- 1 IP address (1 host up) scanned in 24.79 seconds

```

