# This page contains all the stuff learned from JohnHammond's KOTH Videos

## Video 1 : [Link](https://www.youtube.com/watch?v=B7YoMwBYAOU)

Pwncat is awesome. Use it to do a lot of stuff like send and receive files, privesc, etc

```
w
```
The above command is used to check the currently logged in users and their TTYs.
The info like User, IP address and the command executed to get bash is shown there.
If you are root, you can display what commands they type using :
```
cat < /dev/pts/NUMBER
```
Here NUMBER is provided in the output of ** w **

You can spam them by typing:
```
cat /dev/urandom > /dev/pts/NUMBER
```
But do it for very short period of time

Use ** wall ** to write message to other users

#### Squid Proxy

#### Cowsay

#### lolcat

#### terminal-parrot

#### screen

#### nyancat

This occupies the terminal with a cat running

#### cmatrix

Matrix movie like effect on the terminal

#### sl (steam locomotive)

#### Forkbomb
```
:(){ :|: & };:
```
Function name(declaration) : 
Function ()
Function Body {}
Run the function :
Pipe it into the next process |:
Run it in the background &
End the function definition ;
Call the above declared function :
