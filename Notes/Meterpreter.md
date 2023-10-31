# Meterpreter
Meterpreter shells launch in memory.  
It operates via DLL injection

Playbook
1. ```sysinfo``` to gather OS info
2. ```getuid``` - Get permissions
3. ```ps```- lists process tree

### Sessions
Running session commands without opening session - ```sessions -C sysinfo -i 1```  
Kill session - ```sessions -k 1```  
name session - ```sessions -n (name) -i 1```  

### Native Shell
1. In Meterpreter, type ```shell```
2. ```/bin/bash -i```
