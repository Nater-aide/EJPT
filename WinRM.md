# Exploiting Windows Remote Management

WinRM is not enabled by default  
This protocol could manage systems over http or https  
WinRM Ports: 5985 and 5986  

Tools:  
**Crackmapexec** - This will perform a brute-force on winRM to identify users and passwords

**evil-winrm** -- this can obtain a shell session

## Performing Brute force attack with Crackmapexec  
```crackmapexec (protocol) (Target IP) -u (Username / word list) -p (password wordlist)```
