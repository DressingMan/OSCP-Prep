## Linux

```bash
# linpeas / sudo -l / SUID / cron / capabilities
sudo -l
find / -perm -4000 -type f 2>/dev/null
```

## Windows

```powershell
whoami /all
net user
# winPEAS / Seatbelt / interesting services
```
