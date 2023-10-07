# Dotnet Command Line Cheat-Sheet

Quick reference for common Dotnet stuff

## Versioning

### Get what version of the CLI you have
```
azure --version
```
### Create global.json file
```
dotnet new globaljson --sdk-version 7.0.401
```
### Global.json file
```json
{
    "sdk": {
      "version": "7.0.401"
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
