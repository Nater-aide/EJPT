# Upgrading Non interactive shells

```cat /etc/shells``` -- To find valid login shells  
- ```/bin/bash -i```
- ```bin/sh -i```

**Python**  
Check for Python -- ```python --version```  
```python -c 'import pty; pty.spawn("/bin/bash")'```

**Perl** -- ```perl -e 'exec "/bin/bash";'```  
```perl: exec "/bin/bash";```

**Ruby** -- ruby: exec "/bin/bash"

**Bash** -- ```/bin/bash -i```

After getting a shell. Set the path variable    
1. ```env```
2. ```export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin```
3. ```TERM=xterm```
4. ```export SHELL=bash```
