
```
zip2john file.zip > file.hash
```

```
ssh2hohn id_rsa > id_rsa.hash
```

```
pdf2john file.pdf > pdf.hash
```

```
john --wordlist=/usr/share/wordlists/rockyou.txt sitebackup3.hash
```

```
zip2john sitebackup3.zip > sitebackup3.hash
```

```
john --wordlist=/usr/share/wordlists/rockyou.txt pdf_hash
```

```
john hashes.txt --show
```

```
john --wordlist=/usr/share/wordlists/rockyou.txt hash
```

```
ssh2john id_rsa > ssh.hash
```

```
john --wordlist=/usr/share/wordlists/rockyou.txt ssh.hash
```

```
keepass2john Database.kdbx > keepass.hash
```

```
john --wordlist=/usr/share/wordlists/rockyou.txt --rules=sshRules ssh.hash
```

