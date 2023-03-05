# AZ Command Line Cheat-Sheet

Quick reference for common AZ ACI and Docker Commands

## AZ CLI - Login/Account

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
az account set --subscription "<subscription Id>"
```
## Listing locations and resources / general

### List supported regions for the current subscription.
```
az account list-locations
```
## Resource Groups
### List all my resource groups
```
az resource list
```

### Get what version of the CLI you have
```
azure --version
```

### Get help
```
azure help
```
### Create a Resource group
```
az group create --name myresourcegroup --location eastus
```

### list all the resource groups in a subscription
```
az group list --output table
```
### Permanetly deletes a resource group
```
az group delete --name myResourceGroup
```

## ACR

### Authenticate to Azure Container Registry
```
// Docker Desktop must be running
az acr login -n <registry name>
```

### Build Image and Push to ACR (ACR Tasks)
```
az acr build --registry <container_registry_name> --image webimage .
```

### Import Image from One Subscription to Another
```
az acr login -n <destination ACR>

az acr import \
  --name <destinationRegistry> \
  --source <sourceRegistry>.azurecr.io/<Image:Tag> \
  --username <SourceRegistryUsername> \
  --password <SourceRegistryPassword>
```

