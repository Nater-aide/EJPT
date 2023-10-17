# Alternate Data Streams
Details tab
1. Create text file with notepad
2. Enter basic data in text file ex. "hello world"
3. Right click on file and go to properties
4. Select Details

**Within command prompt**  
```notepad test.txt:secret.txt```

**Hiding executables with command prompt**  
``` type payload.exe > windowsupdate.txt:winpeas.exe``` 

**Launching hidden executable**  
Make a link  from elevated command prompt  
```mlink wupdate.exe C:\temp\windowsupdate.txt:winpeas.exe```
```winupdate.exe``` -- this will execute winpeas

