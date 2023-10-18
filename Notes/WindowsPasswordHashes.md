# Windows Password hashes

**LM (Lanman) hashes**
- defunct
- This is not case sensitive. 
- Hashed with DES.
- Does not include salts
  
**NTLM**
   - Windows Vista and onwards.
   - Doesnt split password into "Chunks"
   - Case sensitive
   - Does not use password salts

**LSASS** - local security authority sub system  
 - responsible for authentication on windows.
 - Tools like mikikatz dump the lsass process
