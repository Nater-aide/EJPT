# Enumeration
1. from command line --```host 
isonate.com```  
2. Check the robots.txt  
3. Check the sitemap
4. Use addon called builtwith
5. Whatweb or Wappalyzer
6. httrack -- this will copy an entire website -- ```sudo apt-get install webhttrack```
7. Whois

# Enumeration Web Apps
1. ```dirb http://(IP address)```
2. send get request with curl -- ```curl -X GET (IP address```
3. Send Head request with curl -- ```curl -l (IP address)```
4. send post request with curl -- ```curl -X POST (IP address)```

# Linux
1. hostname
2. uname -a
3. /proc/version
4. etc/issue
5. ps -- also ps axjf
6. env
7. sudo -l
8. id
9. /etc/passwd
10. history
11. netstat

**Find Command**  
- **find . -name flag1.txt**: find the file named “flag1.txt” in the current directory
- **find /home -name flag1.txt**: find the file names “flag1.txt” in the /home directory
- **find / -perm -u=s -type f 2>/dev/null**: Find files with the SUID bit, which allows us to run the file with a higher privilege level than the current user.
- **find / -writable -type d 2>/dev/null**: Find world-writeable folders
- **find / -perm -222 -type d 2>/dev/null**: Find world-writeable folders
- **find / -perm -o w -type d 2>/dev/null**: Find world-writeable folders
- **find / -type f -perm 0777**: find files with the 777 permissions (files readable, writable, and executable by all users)
- **find / -perm a=x**: find executable files
- **find / -mtime 10**: find files that were modified in the last 10 days
- **find / -atime 10**: find files that were accessed in the last 10 day
- **find / -cmin -60**: find files changed within the last hour (60 minutes)
- **find / -amin -60**: find files accesses within the last hour (60 minutes)

