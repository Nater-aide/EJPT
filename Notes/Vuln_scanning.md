# Vulnerability Scanning with Metasploit

Run Nmap scan -- ```db_nmap -sS -sV -O (Target IP)```  

## SearchSploit
Searching Searchsploit -- ```searchsploit "(name you are looking for)"```  
Finding only metasploit modules -- ```searchsploit "(name you are looking for)" | grep -e "Metasploit"```  

## DB Autopwn plugin
https://github.com/hahwul/metasploit-autopwn  
This is used for easy exploiting and vulnerability attacks  

**Installing**
1. Download from Github -- wget https://raw.githubusercontent.com/hahwul/metasploit-autopwn/master/db_autopwn.rb
2. Move file to the /usr/share.metasploit-framework/plugins
3. ```load db_autopwn```

**Usage**  
- Standard scan -- ```db_autopwn -p -t```
- Target specific ports or services -- ```db_autopwn -p -t -PI 445```

## Analyze command
```analyze``` -- into the msf console and it will give you vulnerable items  
```vulns``` - Gives you vulnerabilites
