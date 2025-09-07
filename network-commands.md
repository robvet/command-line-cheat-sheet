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




### Search for unexpected env var
```
echo $env:<name of suspect variable>
```

### Remove env var
```
Remove-Item Env:<name of env variable>
```


### Get process
```
netstat -ano | findstr :5000
```
### Locked by specific process
```
taskkill /F /PID 18236
taskkill /F /IM dotnet.exe
```

### Kill Everything
```
taskkill /F /IM dotnet.exe 2>nul & taskkill /F /IM airline-complaint-system.exe 2>nul
```

### nslookup
```
nslookup is a DNS (Domain Name System) lookup tool that translates hostnames into IP addresses.
 - Takes a hostname (postgres-playground-sql.postgres.database.azure.com)
 - Queries DNS servers to find the corresponding IP address
 - Shows you the translation and any aliases

 Search hierarchy
 - Local DNS cache - Checks if your computer already knows the answer
 - Your router's DNS server (192.168.1.254 - "dsldevice.aaaaa.net") - Your providers router
 - ISP DNS servers - Provider's DNS servers
 - External authoritative DNS servers - Azure's DNS servers that know about

nslookup postgres-playground-sql.postgres.database.azure.com
```

### Get current IP address
```
Invoke-RestMethod -Uri "https://ifconfig.me/ip"``
```
