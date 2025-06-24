# Dotnet Command Line Cheat-Sheet

Quick reference for common Dotnet stuff

## Versioning

### Get what version of the CLI you have
```
azure --version
```
### Show Installed .NET Runtimes
```
dotnet --list-runtimes
```

### Show Installed .NET SDKs
```
dotnet --list-sdks
```
### Start project
```
dotnet run --project airline-complaint-system.csproj
```

### Create global.json file
```
dotnet new globaljson --sdk-version 7.0.401
```
### Global.json file
```json
{
   {
    "sdk": {
        "version": "8.0.409",
        "rollForward": "latestFeature"
    },
    "msbuild-sdks": {
        "Microsoft.NET.Sdk": "8.0.14"
    }
}
```

## User Secrets

### Add Library
```
dotnet add package Microsoft.Extensions.Configuration.UserSecrets
```

### Add Secrets
```
dotnet user-secrets set "OPENAI_APIKEY" "<your OpenAI API key>"
```
