# Network Commandsn

### Determine the device state 
```
dsregcmd /status
```
### Kill Port/Process In Use
```
#System.IO.IOException: 'Failed to bind to address http://127.0.0.1:5000: address already in use.'

# First, kill all .net processes
taskkill /F /IM dotnet.exe

# Kill any app system processes
taskkill /F /IM airline-complaint-system.exe   

# Verify that port 5000 is free
netstat -ano | findstr ":5000"

# Verify that port 5001 is free
netstat -ano | findstr ":5001"

# Clean the build output 
dotnet clean airline-complaint-system.csproj

# Restart app
dotnet run --project airline-complaint-system.csproj



# Get process
netstat -ano | findstr :5000

# Locked by specific process
taskkill /F /PID 18236

taskkill /F /IM dotnet.exe
```

### Kill Everything
```
taskkill /F /IM dotnet.exe 2>nul & taskkill /F /IM airline-complaint-system.exe 2>nul
```
