# This file contains all the stuff related to Learn Linux room of TryHackMe

## SSH
The format of SSH connections is <user>@<host>

## su
su is a command that allows you to change the user, without logging out and logging back in again. For example if you wanted to switch to shiba2 while you're the user shiba1, you would type su shiba2 . You would then be prompted for a password and if you entered shiba2's password you would then become shiba2

## Shell Operators

### >
Output Redirection
Redirecting output of a program to a file.
This operator erases the previous contents of the file before writing to it.

### >>
Same as >
But appends to the file, instead of erasing it.

### &&
&& allows you to execute a second command after the first one has executed successfully

### &
Background Operator
&& and & are completely DIFFERENT

### $
Denotes Environment Variables
To set/change the values of Environment Variables:
```
export <varname>=<value>
```
While using export, don't use $ before varname

### |
Piping Operator
Used to pipe the output of command1 as an input to command2
```
command1 | command2
```

### ;
As && is analogous to AND, ; is analogous to OR

### chown
The chown command allows us to change the user and group for any file. 
```
chown user:group file
```

### ln
* Hard Linking : Completely Duplicates the file and links the duplicate to the original, ie any changes done to the created link is reflected to the original.

```
ln source destination
```
* Symbolic Link (symlink)
It's a glorified reference, does not contain actual data
```
ln -s source destination
```

### find
Recursively find files 
Find files of specific user
```
find <dir> --user <username>
```


