# EJPT
##Notes and commands cheat sheet for the EJPT


SMBMap

```smbmap -u "(username)" -p "(password)" -H "(IP address)```

Downloading file using SMB Map

```smbmap -u administrator -p smbserver_771 -H 10.4.244.255 --download "c$\flag.txt```

Brute forcing FTP using Hydra

```hydra -L (Username list) -P (Password list) (IP Address) ftp```
