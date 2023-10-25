## SMBMap

Show permissions for user  
```smbmap -u "(username)" -p "(password)" -H "(IP address)```

List out contents of drive  
```smbmap -H (Ip address) -u (username) -p (password) -r C$```

Downloading file using SMB Map  
```smbmap -u administrator -p smbserver_771 -H 10.4.244.255 --download "c$\flag.txt```

Executing a command  
```smbmap -H (Ip address) -u (username) -p (password) -x 'command' ---command example-IPconfig```

## Metasploit

**Modules**:  
**Auxiliary/scanner/smb/smb_enumshares** -- enumerates shares  
**Auxiliary/scanner/smb/smb_login** -- dictionary attack you can use against SMB  
**Auxiliary/scanner/smb/smb_version** -- Checks SMB Version
**Auxiliary/scanner/smb/smb_enumusers** -- enumerate SMB users

## RPCClient

```rpcclient -U "" -N 192.168.0.0```

Useful commanands within
- Enumdomusers
- Lookupnames -- example lookupnames admin

## Connecting to SMB share

```smbclient //(IP Address)/(folder you found) -N```

**get** command -- Getting file

### SMB NMAP scripts

```nmap -p445 --script smb-protocols (IP Address)```  
```nmap -p445 --script smb-security-mode (IP Address)```  
```nmap -p445 --script smb-enum-sessions (IP Address)```  
```nmap -p445 --script smb-enum-shares (IP Address)```  
```nmap -p445 --script smb-enum-domains (IP Address)```  
```nmap -p445 --script smb-enum-groups (IP Address)```  
```nmap -p445 --script smb-enum-services (IP Address)```  
```nmap -p445 --script smb-enum-shares,smb-ls --script-args smbusername=(username),smbpassword=(password) (IP Address)```  
_IPC$ is useful. It is an anonymous session. It allows guest access._
