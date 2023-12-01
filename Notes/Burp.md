# Burp Suite
### Directory Busting
1. Intercept the page using Foxy proxy
2. Send the request to intruder
3. Enter target and port
4. Positions - after get / add **$name%**
5. Attack type -- Sniper
6. Payloads -- add a wordlist
7. Start attack

### Passive Crawling
1. Capture the get request
2. Go to dashboard
3. verify Live Passive Crawl from Proxy is enabled
4. Turn off intercept
5. Navigate the site
6. Go to Target > Site Map
7. This gives us a tree

### Attack basic authentication
1. Intercept the login request
2. Send to intruder
3. Pick your position
4. Set payloads -- wordlist
5. Add a prefix -- ```admin:```
6. Encode with Base64
7. Start Attack
