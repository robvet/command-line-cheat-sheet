# AZ CLI Cheat-Sheet

Quick reference for common AZ ACI and Docker Commands

## ACR
### Build Image and Push to ACR (ACR Tasks)
```
az acr build --registry <container_registry_name> --image webimage .
```
## Logging in

### Login with web (interactively)
```
az login
```

### Login in CLI (username)
```
az login -u myemail@address.com
```

### List accounts
```
az account list --output table
```

### Set subscription
```
az account set --subscription "xxx"
```