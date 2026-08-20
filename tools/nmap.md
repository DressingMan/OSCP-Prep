

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

