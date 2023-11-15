# AV Evasion with Shelter
This process can bypass Antivirus. It is injecting your webshell into executables or files.  

**Signature Based detections**  -- based on hashes and signatures of files. Easy to bypass

**Heuristic-based detection**  -- Relises on rules or decisions to determine whether a binary is malicious. It looks for specifc patters within the code or program calls

**Behaviour based detections**  -- Relies on identifying malware by monitoring its behaviour.

### AV Evasion techniques
- **Obfuscation** -- reorganizing code
- **Encoding** -- changes data to new format. This is easily reversable
- **Packing** -- generates executable with new binary structure with smaller size
- **Crypters** -- ecrypts code or payloads and decrypts the code in memory

### In Memory Evasion techniques
- does not write files to disk
- Injects paylods into a process by leveraging Windows APIs
- Payload is executed in memory in seperate thread

  
