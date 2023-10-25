# Web Server Enumeration

Popular web servers
- Apache
- Nginx
- Microsoft IIS

## Apache

**Modules**  
- **auxiliary/scanner/http/apache_userdir_enum**  -- enumerates for usernames
- **auxiliary/scanner/http/brute_dirs**  
- **auxiliary/scanner/http/dir_scanner**  --directory brute force
- **auxiliary/scanner/http/dir_listing**  
- **auxiliary/scanner/http/http_put**  --
- **auxiliary/scanner/http/files_dir**  -- this will brute force finding files
- **auxiliary/scanner/http/http_login**  -- Brute force to gather login credentials. Make sure to set **Auth_URI** to directory needing login
- **auxiliary/scanner/http/http_header**  -- gets header information
- **auxiliary/scanner/http/http_version**  -- this will print out the version of the webserver on the system
- **auxiliary/scanner/http/robots_txt** -- checks robots.txt file
