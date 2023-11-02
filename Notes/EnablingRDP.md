# Enabling RDP
Remote desktop protocol is typically run on port 3389.  

Requires meterpreter  
Module: **post/windows/manage/enable_rdp**

**Gain access to RDP**
_Requires legitimate credentials_
1. From meterpreter, open a ```shell```
2. ```net users```

**Change password of Admin account** (IOC triggered. Not recommended)  
```net user Administrator (password)```

xfreeRDP
1. From terminal ```xfreerdp /u:Administrator /p:Password1 /v:(targetIP)```
