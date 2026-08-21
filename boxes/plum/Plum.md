
```
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http Apache httpd 2.4.56 ((Debian))
|_http-title: PluXml - Blog or CMS, XML powered !
```

admin : admin
https://github.com/MoritzHuppert/CVE-2022-25018/blob/main/CVE-2022-25018.pdf
uploaded php reverse shell from pentest monkey 

Privesc ->
- cat /var/mail/www-data -> roots password 
- ssh in
