

```
nmap --top-ports 100 -sU $IP
```

```
nmap -Pn -p161 -sU -sV TARGET
```

```
nmap -p161 -sU -A TARGET
```

```
nmap --script=smb-vuln* -p 139,445 $IP
```

```
nmap -p- -sV -sC -vvv $IP --open -oN nmap
```

```
nmap --top-ports 100 -sU $IP
```

```
nmap -sU $IP
```

```
nmap --script=smb-enum-shares $IP
```

```
nmap --script "ldap* and not brute" $ip -p 389 -v -Pn -sT
```

```
nmap --script "ldap*" TARGET -p 389 -v -Pn -sT
```

```
nmap -p 88 --script krb5-enum-users --script-args krb5-enum-users.realm='nara-security.com' TARGET
```

```
nmap --script vuln $IP
```

```
nmap -sU -p161 --script *snmp* $target
```

```
nmap -Pn -p161 -sU -sV TARGET
```

```
nmap -p- -sV -sC $IP --open -oN nmap
```

```
nmap -p- -sU $IP
```

```
sudo nmap -sV -p 443 --script "vuln" TARGET
```

```
nmap TARGET
```

```
nmap -p 1-65535 TARGET
```

```
sudo nmap -sS TARGET
```

```
nmap -sT TARGET
```

```
sudo nmap -sU TARGET
```

```
sudo nmap -sU -sS TARGET
```

```
nmap -sn TARGET-253
```

```
nmap -v -sn TARGET-253 -oG ping-sweep.txt
```

```
nmap -p 80 TARGET-253 -oG web-sweep.txt
```

```
nmap -sT -A --top-ports=20 TARGET-253 -oG top-port-sweep.txt
```

```
sudo nmap -O TARGET --osscan-guess
```

```
nmap -sT -A TARGET
```

```
nmap --script http-headers TARGET
```

```
nmap --script http-title TARGET/24
```

```
nmap --script-help http-headers
```

```
nmap -v -p 139,445 -oG smb.txt TARGET-254
```

```
nmap -v -p 139,445 --script smb-os-discovery TARGET
```

```
sudo nmap -sU --open -p 161 TARGET-254 -oG open-snmp.txt
```

```
sudo nmap -p80  -sV TARGET
```

```
sudo nmap -p80 --script=http-enum TARGET
```

```
nmap -vvv --top-ports 100 -sU $IP -oN nmap_udp
```

```
nmap --interactive
```

```
nmap> !sh
```

```
nmap -p 3306 --script mysql-* $IP
```

```
nmap -p- -sT -sV -A $IP
```

```
nmap -p- -sC -sV $IP --open
```

```
nmap -p- --script=vuln $IP
```

```
nmap --script http-methods --script-args http-methods.url-path='/website'
```

```
nmap -p80,443 --script=http-methods  --script-args http-methods.url-path='/directory/goes/here'
```

```
nmap --top-ports 10 -sU $IP
```

```
nmap -n -sV -Pn -script "ldap* and not brute" TARGET
```

```
sudo nmap   TARGET -p- -sS -sV
```

```
sudo nmap -sV  --script "vuln" TARGET
```

```
sudo nmap -sV -p 443 --script "http-vuln-cve2021-41773" TARGET
```

```
sudo nmap --script-updatedb
```

```
sudo nmap -sC -sV -oN mailsrv1/nmap TARGET
```

```
sudo nmap -sC -sV -oN websrv1/nmap TARGET
```

```
nmap --script-help=clamav-exec.nse
```

```
nmap -sS TARGET-152 -oG text.txt
```

```
nmap --script http-methods --script-args http-methods.url-path='/website'
--script smb-enum-shares
```

