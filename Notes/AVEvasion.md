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

## Shellter
**shellterproject.com**  
This is a shellcode injection tool  
**Install**   
```sudo apt-get install shellter -y```  
THIS IS A WINDOWS EXECUTABLE. YOU WILL NEED WINE IN LINUX  
Install Wine -- ```sudo dpkg--add-architecture i386```  
```sudo apt-get install wine32```  

**Launching**
Folder -- /usr/share/windows-resources/shellter  
```sudo win shellter.exe```

**Injecting**
Try to inject into small executable such as winrar  
/usr/share/windows-binaries  
Program to use -- vncviewer.exe  
Launch shellter -- ```sudo wine shellter.exe```  
choose A for auto  
Enter PE target -- path to executable  
Enable stealth mode -- whether you want the executable to function as intended  
Choose your payload - C=customer L=listed payload


