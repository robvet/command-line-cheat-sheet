## Azure ContrainerApp CLI Commands

### CLI Reference
```
https://learn.microsoft.com/en-us/cli/azure/reference-index?view=azure-cli-latest
```

### Open SSH shell into running container app 
```
# exec into runing app with bash shell
az containerapp exec -n MyContainerapp -g MyResourceGroup --command bash

# exec into runing app
az containerapp exec -n MyContainerapp -g MyResourceGroup

# exec into a particular container app replica and revision
az containerapp exec -n MyContainerapp -g MyResourceGroup --replica MyReplica --revision MyRevision
```

# disable a container app
az containerapp revision deactivate -g <resource group> --revision <container app revision>

# reactivate (enable) disabled container app
az containerapp revision activate -g <resource group> --revision <container app revision>

