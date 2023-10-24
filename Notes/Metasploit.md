# Metasploit

Modules -- piece of code that can be executed by MSF
1. **Exploit** - Used to take advantage of vulnerability. Paired with payload
2. **Payloads** - Piece of code delivered to target system
    - Non Staged - Sent as whole
    - Staged - Sent in two parts. Stager and Stage
3. **Encoders** - Used for evading AV detection
4. **NOP** - This ensures that payload sizes are consistent and ensure the stability of a payload when executed
5. **Auxiliary** - Port scanning and Enumeration

**Meterpreter** - advanced multi-functional payload. Executed in memory

**Directories**  
/usr/share/metasploit-framework  
Modules - /usr/share/metasploit-framework/modules

**Metasploit Database**  
The database keeps track of your assessments  
It uses Postgresql as its primary database  
It facilitates the importation and storage of scan results from 3rd party tools like Nmap and Nessus  
```sudo systemctl enable postgresql``` -- this will start the service on system startup  
```sudo systemstc start postgresql``` -- starts the service immediately  
```sudo msfdb``` --this allows you to manage the database  
```sudo msfdb init``` -initializes database
