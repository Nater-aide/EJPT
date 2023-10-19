# FTP

**Brute Force Login**   
```hydra -L (username) -P (password list) (IP address) ftp```  
Check for anonymous logins

**FTP Nmap scripts**  
```ls -al /usr/share/nmap/scripts | grep ftp-*```

**Searchsploit**  
Search for version of FTP and locate exploits available  
_make sure to check for version_

# SSH

**Metasploit Modules**:  
auxiliary/scanner/ssh/ssh_version  
auxiliary/scanner/ssh/ssh_login

**Brute Force login**  
```hydra -L /usr/share/metasploit-framework/data/wordlists/common_users.txt -P /usr/share/metasploit-framework/data/wordlists/common_passwords.txt (target IP) -t 4 ssh```

