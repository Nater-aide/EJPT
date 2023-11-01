# Bypassing UAC using Metasploit
UAC Bypass: Memory Injection

A specific payload is required for bypassing UAC  
Payload: **windows/x64/meterpreter/reverse_tcp**  

The account you are logged into needs to be an admin  
1. Background meterpreter
2. Module -- **exploit/windows/local/bypassuac_injection**
3. if fails, ```set TARGET (press tab or options)```
4. Run ```getsystem``` to upgrade privileges
