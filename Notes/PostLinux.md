# Linux post exploitation
Get a bash session

get shell
- ```/bin/bash -i```
- ```cat /etc/passwd```
- get group info ```groups root```
- get kernel version ```uname -r```
- list out processes - ```ps aux```
- enumerate environment variables -- ```env```

### Meterpreter
- **post/linux/gather/enum_configs** -- retrieves linux config files
- **post/multi/gather/env** -- 
- **post/linux/gather/enum_network** -- 
- **post/linux/gather/enum_protections** -- Gathers protection enumeration. This stores in notes. ```notes``` command shows you info you've gathered
- **post/linux/gather/enum_system** -- system and user enumeration.
- **post/linux/gather/checkcontainer** -- checks if this is a container 
- **post/linux/gather/checkvm** -- Checks if this is a VM
- **post/linux/gather/enum_users_history** -- Enumerates user's history
- **post/multi/manage/system_session** -- 
- **post/linux/manage/download_exec** -- 
