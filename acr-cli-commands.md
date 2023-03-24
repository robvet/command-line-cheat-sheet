# AZ ACR CLI Command Line Cheat-Sheet

Quick reference for common AZ ACR CLI Commands

## ACR

### Authenticate to Azure Container Registry
```
// Docker Desktop must be running
az acr login -n <registry name>
```

### Build Image and Push to ACR (ACR Tasks)
```
az acr build --registry <container_registry_name> --image <name the image>:<provide tag> .
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
