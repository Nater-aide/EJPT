# Enumerating System Information post enumeration
- What are we looking for
  - hostname
  - os name
  - os build
  - os architecture
  - installed updates/hotfixes

Get user information -- ```getuid```  
get system info -- ```sysinfo```  
Get everything (from shell) -- ```systeminfo```  

Check c:\Windows\System32\eula.txt  
This can provide information for the OS version and build number

```wmic qfe get Caption,Description,HotFixID,InstalledOn``` -- enumerates list of installed updates in addition to hotfix URL

# Enumerating Users & Groups
- What are we looking for
 - Current user and privs
 - Additional user information
 - groups
 - Members of the built in admin group

Get user information -- ```getuid```  
Get priviliges -- ```getprivs```
currently logged on users -- module:**enum_logged_on_users**

**From shell**
- whoami  
- whoami /priv  
- query user -- tells us the currently logged on user  
- net users -- display all of the accounts on the system
- net user (username) -- tells you more info about the account
- Net localgroup -- shows all the local groups on the system
- net localgroup (username) -- gives groups the user is a part of
