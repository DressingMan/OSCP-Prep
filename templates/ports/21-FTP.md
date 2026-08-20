## NMAP

```bash
nmap -sV -sC -p 21 TARGET
```

## Enum

```bash
ftp TARGET
# try anonymous / anonymous

hydra -C /usr/share/seclists/Passwords/Default-Credentials/ftp-betterdefaultpasslist.txt TARGET ftp
```
