# This file contains some tips and tricks to solve the challenges

## ASM Challenges
If the given challenge is an ASM File, try to compile it using nasm and then reverse it using any RE Framework, or write a C program and compile it with -S flag to result a .s file, mind the arch and Big/Little Endian formats, and replace the assembly code.

## Random
```
Whenever Schrodinger comes into reference, always use cat
```
```
For viewing the differences between the contents of the two folders, use grep -R . from the first directory and send it to a text file in the parent directory. Do the same for the other folder. Apply diff command to both text files. Grepping from the parent folder will include the folder name of both folders, which will result in all lines of all files being different.
```
## Spawn a regular Shell using Python
```
python -c 'import pty;pty.spawn("/bin/bash")'
```
To get a persistent shell, you need a reverse shell. Best source - PentestMonkey
Also, php reverse shell is present in kali. Just locate it.

To give tab autocomplete to the created shell...
```
stty raw -echo
< Press Enter >
fg
< Press Enter Twice >
```
enchant python library consists inbuilt dictionary
qrencode 
rainbowstream API to post to twitter
jadx-gui

## Search in the man page by typing /SEARCHQUERY
