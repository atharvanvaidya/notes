# This file contains all the stuff learned from the Volatility Room

Volatility is a free memory forensics tool developed and maintained by Volatility labs. 
Volatility is wildly expandable via a plugins system and is an invaluable tool for any Blue Teamer.

## Obtaining Memory Capture

* FTK Imager -
* Redline - Link *Requires registration but Redline has a very nice GUI
* DumpIt.exe
* win32dd.exe / win64dd.exe - *Has fantastic psexec support, great for IT departments if your EDR solution doesn't support this

hiberfil.sys, better known as the Windows hibernation file contains a compressed memory image from the previous boot. Microsoft Windows systems use this in order to provide faster boot-up times
Location : %SystemDrive%/hiberfil.sys

## Volatility Commands

Access the hidden processes by using the command psxview

View active connections using netscan

ldrmodules. Three columns will appear here in the middle, InLoad, InInit, InMem. If any of these are false, that module has likely been injected which is a really bad thing. On a normal system the grep statement above should return no output.

Using the 'apihooks' command we can view unexpected patches in the standard system DLLs. If we see an instance where Hooking module: < unknown > that's really bad.

malfind is used to find the injected (potential malicious) code and dump it into the specified directory : 
```
volatility -f MEMORY_FILE.raw --profile=PROFILE malfind -D <Destination Directory>
```

dlllist - View all of the DLLs loaded into memory. DLLs are shared system libraries utilized in system processes. These are commonly subjected to hijacking and other side-loading attacks.

## Links

* [Virus Total](https://www.virustotal.com/gui/home/upload)
* [Hybrid Analysis](https://www.hybrid-analysis.com/)
* [AlienVault Open Threat Exchange (OTX)](https://otx.alienvault.com/)
* FOR500 Sans Windows Forensics Analysis

