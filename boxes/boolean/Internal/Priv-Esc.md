
![Pasted image 20240716174804.png](Evidence/Pasted%20image%2020240716174804.png)

discovered a root private key in remis .ssh folder 

![Pasted image 20240716180648.png](Evidence/Pasted%20image%2020240716180648.png)

![Pasted image 20240716180707.png](Evidence/Pasted%20image%2020240716180707.png)

tried to ssh into root @ localhost but I got an error 

https://stackoverflow.com/questions/75890387/ssh-too-many-authentication-failures

after researching the error on stack-overflow I found extra parameters that somehow worked 

```
ssh -i root root@127.0.0.1 -o IdentitiesOnly=yes
```

![Pasted image 20240716180733.png](Evidence/Pasted%20image%2020240716180733.png)

![Pasted image 20240716181005.png](Evidence/Pasted%20image%2020240716181005.png)

**Lessons learned ->** 
if you get a "Too many authenication failuers" error use the parameter above or the other one in the link above to stack-overflow

