
```
ldapsearch -v -x -b 'dc=hutch,dc=offsec' -H 'ldap://TARGET' '(objectclass=*)' > ldap_search.txt
```


```
kerbrute -domain hutch.offsec -users ./users.txt -dc-ip TARGET
```
Confirming that all the users are valid 


## LDAPsearch

```
ldapsearch -v -x -b 'dc=hutch,dc=offsec' -H 'ldap://TARGET' '(objectclass=*)' > ldap_search.txt
```

```
cat ldap_search.txt | grep -i "samaccountname"\
```
To get all the users 

```
cat raw_users.txt | cut -d: -f2 | tr -d " " > users.txt
```

```
kerbrute -domain hutch.offsec -users ./users.txt -dc-ip TARGET
```
Confirming that all the users are valid 

```
cat ldap_search.txt | grep -i description
```

```
crackmapexec smb TARGET -u ./users.txt -p ./passwords.txt --continue-on-success
```


```
ldapsearch -x -H ldap://$IP -b “dc=access,dc=offsec”
```
Operations error = needs creds
```
ldapsearch -x -H ldap://$IP -b “dc=access,dc=offsec” -w <password>
```


```
ldapsearch -v -x -b "DC=hutch,DC=offsec" -H "ldap://TARGET" "(objectclass=*)"
```

```
ldapsearch -x -h TARGET -b "dc=hutch,dc=offsec" > ldap_search.txt
```

```
ldapsearch -x -H ldap://$ip -b “dc=Kyotosoft,DC=com”
```

```
kerbrute -domain hutch.offsec -users ./users.txt -dc-ip TARGET
```

```
./kerbrute userenum -d resourced users --dc TARGET
```

```
cat ldap_search.txt | grep -i "samaccountname"
```

```
cat raw_users.txt | cut -d: -f2 | tr -d " " > users.txt
```