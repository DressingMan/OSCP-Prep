upgrade shell to a tty 

![Pasted image 20240712143116.png](Evidence/Pasted%20image%2020240712143116.png)

![Pasted image 20240712145616.png](Evidence/Pasted%20image%2020240712145616.png)

`dora : doraemon`

let switch users 

![Pasted image 20240712145808.png](Evidence/Pasted%20image%2020240712145808.png)

we are now dora 

![Pasted image 20240712145856.png](Evidence/Pasted%20image%2020240712145856.png)

dora is in the disk group

![Pasted image 20240712150313.png](Evidence/Pasted%20image%2020240712150313.png)

with `debugfs` we can read files with root permissions 

![Pasted image 20240712150445.png](Evidence/Pasted%20image%2020240712150445.png)

we can read the entire /etc/shadow file containing roots hashed password 

![Pasted image 20240712150558.png](Evidence/Pasted%20image%2020240712150558.png)

we cracked roots password with john now we can su aka switch user to root

![Pasted image 20240712150644.png](Evidence/Pasted%20image%2020240712150644.png)

![Pasted image 20240712150715.png](Evidence/Pasted%20image%2020240712150715.png)

