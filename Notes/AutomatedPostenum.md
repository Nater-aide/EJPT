# Automating Windows Local Enumeration
_Enumerate all systems connected to same network_  
Module: post/windows/gather/enum_computers  

_Enumerate installed application_  
module: post/gather/enum_applications

_Enumerate patches_  
module: post/gather/enum_patches

### JAWS - Just another Windows Enum Script
https://github.com/411Hall/JAWS  
This is designed in Powershell

Getting started
1. Download the PS1 script (or copy it)
2. Upload to target host using the ```Upload``` command
3. type ```shell``` to get a shell
4. Execute script -- ```powershell.exe -ExecutionPolicy bypass -File jaws-enum.ps1 -OutputFileName JAWS-Enum.txt```

