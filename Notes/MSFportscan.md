# Port scanning with auxiliary modules

Auxiliary modules will allow you to port scan to another host while connected to a compromised host.  
This will allow you to pivot to another host on a network. Allows you to access hosts on a private network.

### From Meterpreter Session

Finding the private network IP
1. open shell -- ```shell```
2. Spawn bash session -- ```/bin/bash -i```
3. Get internal IP -- ```ifconfig```
4. Add Route to meterpreter -- ```run autoroute -s 192.255.78.2```  
   - _You just need to provide internal IP address. Subnet not needed_
5. Background meterpreter session -- ```background```
6. Search portscan and use the TCP port scanner
7. Set options with new IP address

**UDP Scan**  
Module: UDP_Sweep  
Only need to set the RHOSTS option
