# Clearing your tracks on Windows
When running metasploit modules, pay close attention to any artifacts that may be generated.  
Deleting Windows Event log. This is something that should be avoided completely.  
Run as much as you can from the temp folder so that you can delete easier  

**Bad Blue (and other modules in MSF)**  
1. ```show advanced``` - this will show what the module does
2. ```show info``` -- info may tell you the files it creates

Some modules have resource scripts that will remove everything for you  
run resource script -- ```resource (path to the resource script)```

```clearev``` -- Deletes windows event logs
# Clearing your tracks on Linux
Linux machines may require more manual cleanup as opposed to resource scripts  
Check the users .bash_history file

If there, you can delete the content -- ```history -c``` or ```cat /dev/null > .bash_history```
