# Keylogging

Keylogging is capturing keyboard strokes  
Meterpreter allows us to capture keystrokes  

1. Get a meterpreter shell
2. migrate to explorer.exe process -- keylogging works best with the explorer process
3. ```pgrep explorer```

Commands to utilize
- **keyscan_dump**   Dump the keystroke buffer
- **keyscan_start**  Start capturing keystrokes
- **keyscan_stop**   Stop capturing keystrokes
