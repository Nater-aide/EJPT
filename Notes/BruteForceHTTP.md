# Brute Forcing HTTP logins with Hydra
1. enter fake login information info the login form
2. copy the error message that is received
3. Go to the page source and check into the data below

hydra -L usernames -P passwords 192.208.137.3 http-post-form"/login.php:login=^USER^&password=^PASS^&security_level=0&form=submit:Invalid credentials or user not activated!"

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

# Brute force logins with Burp
1. Navigate to login page
2. Enable Foxy proxy
3. Launch Burp
4. Login with fake credentials
5. Send to intruder
6. Enter Target and Port (leave default if it is correct)
7. Click Positions tab
8. If encoded, right click on the information, select convert selection>Base64 decode
9. replace the credentials with a parameter that is going to be substituded. Example: the word **creds**
10. Highlight the word and select "Add $"
11. Click payloads tab
12. Load your password list
13. Click Payload process and select Add
14. Add prefix
15. enter admin: (or whatever username you would like to test)
16. Select add again under payload processing and choose encode
17. Base64 encode
18. Click start attack
19. Looks for status code with a different code
20. Choose the odd man out
21. Right click and send to decoder
