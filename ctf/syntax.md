# This file contains the basic syntax of some daily usage tools 

## grep
```
grep -R <pattern> -> Search recursively for patterns in the current directory
```

## dd (disk digger)
```
dd bs= < NoOfBytesToRead > skip= < skipBytesInDecimal > count= < BytesOffsetInDecimal > if= < NameOfInputFile > of= < NameOfOutputFile >
```

## ssh with private key
```
ssh -i PRIVATEkEYFILE USERNAME@IPADDRESS
```

## Tmux attach
```
tmux -S default attach
```

## Search logs from terminal
```
ausearch
```

## Convert the GIF into individual images (Requires imagemagick installed)
```
convert FILENAME.gif OUTPUT.png
```

## nmap vuln scan (takes a while to load)
```
nmap -sC -sV -A --script vuln -p- IPADDRESS
```

## dirb scan
```
dirb URL WORDLIST
```
```
dirb URL /etc/share/wordlists/common.txt
```
