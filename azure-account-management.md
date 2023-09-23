# AZ Command Line Cheat-Sheet

Quick reference for common AZ ACI Account Management

## AZ CLI - Login/Account

### Login with web (interactively)
```
az login
az login -u myemail@address.com
az login -t <AAD tenant Id>
```
### Show current AAD User
```
az ad signed-in-user show
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

### Get help
```
azure --help 
azure <command> --help
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
