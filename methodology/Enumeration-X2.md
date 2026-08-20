```bash
export IP=""
```

```bash
nmap -p- -sV -sC -vvv $IP --open -oN nmap
```

```bash
nmap -vvv --top-ports 100 -sU $IP -oN nmap_udp
```

```bash
export URL=""
```

```bash
gobuster dir -u $URL -w /usr/share/SecLists/Discovery/Web-Content/raft-medium-directories.txt -k -t 30 > Dir.txt
```

```bash
gobuster dir -u $URL -w /usr/share/SecLists/Discovery/Web-Content/raft-medium-files.txt -k -t 30 > Files.txt
```

To brute force a login page when you're not getting parameters in burp use this -> 
```bash
hydra -l admin -P /usr/share/wordlists/rockyou.txt http-get://TARGET
```

this is for the http-get!!!
Make sure you're hitting the right port!!!

PWN KIT (Python)

```bash
git clone https://github.com/joeammond/CVE-2021-4034.git
```

