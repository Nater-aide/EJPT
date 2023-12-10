# Brute Forcing HTTP logins with Hydra
1. enter fake login information info the login form
2. copy the error message that is received
3. Go to the page source and check into the data below

```hydra -L usernames -P passwords 
192.208.137.3
 http-post-form"/login.php:login=^USER^&password=^PASS^&security_level=0&form=submit:Invalid credentials or user not activated!"```

https://assets.ine.com/labs/ad-manuals/walkthrough-1895.pdf

# Brute Force HTTP login form with OWASP-ZAP
1. Launch Owasp-Zap
2. click Manual Explore
3. Enter Target IP Address url (http://IP address)
4. Select Launch Browser
5. Continue to your target
6. Attempt to login to your target
7. Check the site map for a post request
8. Click the POST request and select the Request tab
9. Right click the request and select Fuzz
10. Select username and click Add
11. Add your payload (usernames or username list)
12. Do the same for the Password
13. Start Fuzzer
14. Check for any 302 codes.  
