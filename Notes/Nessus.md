# Nessus

Nessus is a vulnerability scanner  
Nessus essentials will is free and will allow us to scan up to 16 hosts  

1. Download from https://www.tenable.com/products/nessus/nessus-essentials  
2. ```chmod +x (filename)```  
3. ```dpkg -i (filename)```

Start Nessus Scanner  -- ```sudo systemctl start nessusd.service```  
Launch in web browser

**Filters**  
Using filters, set Metasploit frame = True  
This will allow you to see if it is vulnerable to Metasploit  
The details within the finding will tell you the Module in Metasploit

## Export Scan and import into Metasploit
1. Click Export in Nessus
2. Save File
3. Launch Metasploit
4. ```db_import /(exported file)```
5. type ```vulns -p (port number)```
6. Search for CVE number
