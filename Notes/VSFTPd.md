# Targetting VSFTPd
1. Check for anonymous logins
2. Brute force logins
3. Check for SMTP enablement -- MSFconsole modile: **smtp_enum**


If there is a dav folder  
1. FTP into the system
2. Upload a reverse shell
3. Navigate to /usr/share/webshells/(Shell type) -- using php for linux
4. cp /usr/share/webshells/php/php-reverse-shell
5. Update information within the shell to your host machine info using text editor
6. make shell executable
7. upload using the put command in FTP in the var/www/dav/ folder on the server

Metasploit Module: **exploit/unix/ftp/vsftpd_234_backdoor**
