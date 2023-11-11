# Netcat
TCP/IP swiss army knife

Banner Grabbing -- ```nc -nv (ip address) (port)``` 
Listener -- ```nc -lnv (ip address) (port)``` 

Sending and receiving files  
**Listening** - ```nc -lvnp 123 > (filename)```  
**Pulling file** -- ```nc -nv (ip address) (port) < (filename)```

