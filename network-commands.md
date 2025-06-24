# Network Commandsn

### Determine the device state 
```
dsregcmd /status
```
### Kill Port/Process In Use
```
#System.IO.IOException: 'Failed to bind to address http://127.0.0.1:5000: address already in use.'
netstat -ano | findstr :5000

# Locked by specific process
taskkill /F /PID 18236
```

