# AZ CLI Cheat-Sheet

Quick reference for common AZ ACI and Docker Commands

## ACR
```
az acr build --registry <container_registry_name> --image webimage .
```
az acr build --registry container-registry-rg --image test:v1 .

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