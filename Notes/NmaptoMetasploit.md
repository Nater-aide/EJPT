### Exporting Nmap scan results to Metasploit

```-oX (name)``` - this exports your nmap scan results into an XML file  

### Importing
Take scan results from previous scan  
```start postgresql start && msfconsole```  
Create new workspace -- ```workspace -a Win2k12```  
Import data to database -- ```db_import /root/(name of file export)```  
To confirm it imported successfull -- ```services```

### From Within Metasploit
Nmap scan that will automatically save -- ```db_nmap -Pn -sV (IP address)```
