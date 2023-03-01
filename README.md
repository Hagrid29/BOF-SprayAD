# BOF - DomainPasswordSpray

A fork of [SprayAD BOF](https://github.com/outflanknl/C2-Tool-Collection/tree/main/BOF/SprayAD). Perform LDAP-based or Kerberos-based password spray using Windows API `LogonUserSSPI`. Skip disabled accounts, locked accounts and large BadPwdCount (if specified).

### Usage

Kerberos-based password spray

```
SprayAD --userlist /tmp/userlist.txt --password P@ssw0rd
```

Skip users that the number of times the user tried to log on with incorrect password larger than 2

```
SprayAD --userlist /tmp/userlist.txt --password P@ssw0rd --MaxBadPwdCount 2
```

LDAP-based password spray

```
SprayAD --userlist /tmp/userlist.txt --password P@ssw0rd --MaxBadPwdCount 2 --authservice ldap
```



### Compile

```linux
cd SOURCE
make
```



### References

+ [SprayAD BOF](https://github.com/outflanknl/C2-Tool-Collection/tree/main/BOF/SprayAD)