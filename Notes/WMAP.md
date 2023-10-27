# Web App Vulnerability Scanning with WMAP
WMAP is a feature rich web app scanner. It can automate web server enumeration.  
It can be loaded directly into Metasploit

```load wmap```  
Commands you can run -- ```wmap_ (then click tab to list out commands)```

1. Add sites -- ```wmap_sites -a (URL or IP)```
2. Setup Targets -- ```wmap_targets -t http://(IP or URL)/```
3. Check for aux modules that would be useful -- ```wmap_run -t```
4. Run scan against target -- ```wmap_run -e```
5. Checking vulnerabilites it was able to detect -- ``wmap_vulns -l```

HTTP put module for upload testing  
use **auxiliary/scanner/http/http_put**  
