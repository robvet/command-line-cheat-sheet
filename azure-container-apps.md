## Azure ContrainerApp CLI Commands

### CLI Reference
```
https://learn.microsoft.com/en-us/cli/azure/reference-index?view=azure-cli-latest
```

### Install the Azure Container Apps extension for the CLI
```
az extension add --name containerapp --upgrade
```

### Register the Microsoft.App namespace
```
az containerapp update --name ca-web-xxx  --resource-group rg-xxx --set tags.forceRestart=$(Get-Date -Format o)
```

### Fetch ALL environmental vars
```
az containerapp show --name ca-web-ragxxx --resource-group xxx  --query "properties.template.containers[0].env"
```

### Open SSH shell into running container app 
```
# exec into runing app with bash shell
az containerapp exec -n MyContainerapp -g MyResourceGroup --command bash

# exec into runing app
az containerapp exec -n MyContainerapp -g MyResourceGroup

##exec into a particular container app replica and revision
az containerapp exec -n MyContainerapp -g MyResourceGroup --replica MyReplica --revision MyRevision
```

### Disable container app
```
# disable
az containerapp revision deactivate -g <resourceGroup> --revision <containerAppRevision>

# reactivate (enable) disabled container app
az containerapp revision activate -g <resourceGroup> --revision <containerAppRevision>
```

### Restart container app
```
az containerapp update --name ca-web-xxxx  --resource-group rg-xxxx --set tags.forceRestart=$(date -Iseconds)
```

### Change Environment Variable value
```
az containerapp update --name ca-web-ragapp --resource-group rg-blah --set-env-vars AZURE_SEARCH_INDEX=desginwins
```
