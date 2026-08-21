
```
www-data@ubuntu:/var/www/html/console$ sudo -l
sudo -l
Matching Defaults entries for www-data on ubuntu:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User www-data may run the following commands on ubuntu:
    (ALL) NOPASSWD: /bin/systemctl start apache2
    (ALL) NOPASSWD: /bin/systemctl stop apache2
    (ALL) NOPASSWD: /bin/systemctl restart apache2
www-data@ubuntu:/var/www/html/console$
```

This is changing who is running the apache2 web engine service 
This changes who owns it and who group owns it 
That way when you get back into the machine, the you'll get in as the user who owns it and group owns it

```
cp /etc/apache2/apache2.conf .
```
```
sed -i 's/User ${APACHE_RUN_USER}/User mahakal/g' apache2.conf
```
```
sed -i 's/Group ${APACHE_RUN_GROUP}/Group mahakal/g' apache2.conf
```
```
cp apache2.conf /etc/apache2/apache2.conf
```
```
sudo /bin/systemctl restart apache2
```

