# Clue

Sanitized practice-box notes. Folder layout matches the Obsidian template: **General Info → External (per port) → Exploit → Internal / Priv Esc → Loot**, with **Evidence** next to the phase where the screenshot was taken.

| | |
| --- | --- |
| OS (guess from ports) | Linux |
| Notes | Personal walkthrough, not a spoiler-free writeup |

## Layout

- [General Info](General-Info.md)
- [Exploit](Exploit.md)
- [Loot](Loot.md)
- [External](External/) — per-port enumeration
- [Internal / Priv Esc](Internal/Priv-Esc.md)

### Ports touched

- `139-netbios-ssn`
- `22-ssh`
- `3000-http`
- `80-http`
- `8021-freeswitch-event`

## Attack notes

check to see who can ssh in -> /etc/ssh/sshd_config cassie : SecondBiteTheApple330 I reasearched to find out how to change the event_socket password... it told me this directory is where the password is stored -> `/etc/freeswitch/autoload_configs/event_socket.conf.xml` I tried it in smb but it came back as the default password.... So I tried it with the remote file read exploit from cassandra. and what do you know, I have another password!!!! StrongClueConEight021 Now I can plug this into the other exploit that I found for freeswitch -> https://www.exploit-db.com/exploits/47799 I had to modify the exploit code in order to successfully authenticate... and we have command execution on the target! time for a reverse shell

### Commands used

```bash
/etc/ssh/sshd_config
cassie : SecondBiteTheApple330
StrongClueConEight021
curl --path-as-is http://TARGET:3000/../../../../../../../../etc/passwd
sudo -u root /usr/local/bin/cassandra-web -B 0.0.0.0:9999 -u cassie -p SecondBiteTheApple330
```


### References

- https://www.exploit-db.com/exploits/49362
- https://www.exploit-db.com/exploits/47799

## Evidence

![Pasted image 20240622142801.png](Evidence/Pasted%20image%2020240622142801.png)

![Pasted image 20240622140625.png](Evidence/Pasted%20image%2020240622140625.png)

![Pasted image 20240622140816.png](Evidence/Pasted%20image%2020240622140816.png)

![Pasted image 20240622141458.png](Evidence/Pasted%20image%2020240622141458.png)

![Pasted image 20240621172731.png](Evidence/Pasted%20image%2020240621172731.png)

![Pasted image 20240621172250.png](Evidence/Pasted%20image%2020240621172250.png)

![Pasted image 20240622140714.png](Evidence/Pasted%20image%2020240622140714.png)

![Pasted image 20240622141340.png](Evidence/Pasted%20image%2020240622141340.png)

![Pasted image 20240622150917.png](Internal/Evidence/Pasted%20image%2020240622150917.png)

![Pasted image 20240622144633.png](Internal/Evidence/Pasted%20image%2020240622144633.png)

![Pasted image 20240622143117.png](Internal/Evidence/Pasted%20image%2020240622143117.png)

![Pasted image 20240622150409.png](Internal/Evidence/Pasted%20image%2020240622150409.png)
