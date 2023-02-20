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
az acr login -n <registry name>
```

### Build Image and Push to ACR (ACR Tasks)
```
az acr build --registry <container_registry_name> --image webimage .
```

## AKS

### Get credentials and clear cache
```
az aks get-credentials -g <resource group> -n <aks cluster> --overwrite-existing
```

### Port-forward -- Invoke POD with a private clusterIP address
```
kubectl port-forward <running POD> 8080:8080   # <host port>:<container port>
```

### Get events from troubleshooting
```
kubectl get events -n api <--sort-by>
Kubectl get endpoints
kubectl describe resourceType/name 
kubectl logs runningPodName
```

### Execute a command inside a running container
```
kubectl exec -it <podname> -n api -- /bin/sh
curl http://localhost/<some url>

docker exec sql /opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P '<password>' -Q "SELECT NAME FROM sys.databases"
```

### Stop (disable) cluster when not in use -- optimze costs
```
az aks stop -g <resource group> -n <aks cluster>

# Confirm VM has stopped - powerState: stopped 
az aks show -g <resource group> -n <aks cluster>

# Restart cluster VM
az start stop -g <resource group> -n <aks cluster>
```



