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