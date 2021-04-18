# Windows : Bastion : HackTheBox

[Video Link](https://www.youtube.com/watch?v=2j3FNp5pjQ4&list=PLidcsTyj9JXL4Jv6u9qi8TcUgsNoKKHNn&index=2)

List all files from a .vhd file
```
7z -l FILENAME.vhd
```

Tools related to the SMB
* guestmount
* smbclient
* smbmap
SAM Hashes
```
USER: :LM:NTLM:
```
If LM hashes start with aad3, they are blank
Similarly with NTLM hashes starting with 31d6

If both the hashes are blank for administrator, then it is probable that the account is disabled.
For other users, the password does not exist!

[Check NTLM Hashes online](https://hashes.org)

## JAWS Windows Enumeration Tool

## SMBmap
```
smbmap -u USERNAME -p PASSWORD -H IPADDRESS
```
