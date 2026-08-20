

To read a file that you don't have user access to, but you have the abilty to use TAR as an user use this ->

This will copy the file
```
./tar -cf pass.tar /var/backups/.old_pass.bak
```

This will extract it
```
./tar -xf pass.tar
```

Then cat the file!

