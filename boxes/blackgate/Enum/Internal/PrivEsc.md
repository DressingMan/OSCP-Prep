![Pasted image 20240610223634.png](Evidence/Pasted%20image%2020240610223634.png)

![Pasted image 20240610223756.png](Evidence/Pasted%20image%2020240610223756.png)

![Pasted image 20240610223848.png](Evidence/Pasted%20image%2020240610223848.png)


Upon running strings on the binary in the sudoers file, I found a authorizations key hard-coded into the binary.

Authorizations key ->
```
ClimbingParrotKickingDonkey321
```

![Pasted image 20240610224417.png](Evidence/Pasted%20image%2020240610224417.png)

I put in the key, then it gave me a nano prompt, i used `!sh` to get out of it, and I became root.

![Pasted image 20240610224320.png](Evidence/Pasted%20image%2020240610224320.png)

