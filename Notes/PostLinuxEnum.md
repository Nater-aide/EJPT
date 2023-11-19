# Linux Local enumeration
What are we looking for
- hostname
- Distribution
- Kernel Version
- CPU info
- Disk Usage
- Installed packages / software

# Enumeration network information
Commands  
- ifconfig
- ip a s -- interface info. Similar to ifconfig. Where you find other devices you can pivot to
- netstat -- interested in the established session
- route -- displays routing table. Interested in gateway
- cat /etc/networks -- if ifocnfig is not installed
- cat /etc/resolve.conf
- arp -a
- 
