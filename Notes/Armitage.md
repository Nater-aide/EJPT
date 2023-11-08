# Armitage
Armitage is a GUI interface for Metasploit  
Provides you with the ability to visualize the targets  

Launching Armitage
1. ```servicepostgresql start && msfconsole```  
2. New terminal, type ```armitage```
3. press connect
4. start RPC server

### Pivoting
1. Right click on host and select Pivtoing>setup  
2. Select Services
3. go to meterpreter session that is open. Port forward 80 to 1234 using ```portfwd add -l 1234 -p 80 -r (target IP)```
4. go to host (not meterpreter) and run ```db_nmap -sV (target IP) -p 1234 localhost
5. 
