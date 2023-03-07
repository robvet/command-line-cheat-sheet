## AKS Commands (both Azure CLI and Kubectl)

### Great reference
```
https://kubernetes.io/docs/reference/kubectl/cheatsheet/
```

### Install Kubectl 
```
# Download client to /usr/local/bin/kubectl
az aks install-cli
```

### Get credentials and clear cache
```
az aks get-credentials -g <resource group> -n <aks cluster> --overwrite-existing
```

### Invoke ClusterInfo Kubernetes Tool
```
# OUTSTANDING Kuberentes Visual Tool by Mark Kiznerman: https://github.com/scubakiz/clusterinfo
kubectl port-forward svc/clusterinfo 5252:5252 -n clusterinfo
```
### Query the cluster nodes
```
# Show nodes, but not the availability zones (if provisioned)
kubectl get nodes

# Complex query to see each node and its corresponding availability zone
kubectl get nodes -o custom-columns=NAME:'{.metadata.name}',REGION:'{.metadata.labels.topology\.kubernetes\.io/region}',ZONE:'{metadata.labels.topology\.kubernetes\.io/zone}'
```

### Trobuleshoot 
```
# Pods
kubectl describe pod <pod name>
kubectl log <podname>
```

### Include all K8s namespaces parameter (beyond default namespace)
```
// Shows objects outside of default namespace
kubectl get pods --all-namespaces 

// Short version of command
kubectl get pods -A
```

### Scale
```
# Nodes
az aks nodepool scale -g <Resource Group name> --cluster-name <AKS Cluster name> --name <Name of AKS Nodepool> --node-count 1
```

### Watch cluster events
```
kubectl get events --sort-by='{.lastTimestamp}' --watch
```

### Trobuleshoot 
```
# Pods
kubectl describe pod <pod name>
kubectl log <

### Open 'AKS Workloads' portal view from command line
```
// Opens AKS portal in web browser
aks browse --name <AKS Cluster Name> --resource-group <Resource Group Name>
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
kubectl exec -it <podname> -- /bin/bash

# Once inside, call a resource  
curl http://localhost:<port>/<some url>
  
# Execute into a Mongo DB instance
kubectl exec -it <mongo pod name> -- mongosh "--version"
  
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

### Create yaml file
```
# Kubectl will output a base yaml file without instantiating a container
kubectl run <some name> --image=<ACR Name>.azurecr.io/<Image Name>:<tag> --dry-run=client -oyaml > yaml_file
```

### Integrate ACR Regsitry with an AKS Cluster
```
# Attach ACR Regsitry to an Existing AKS Cluser
$ az aks update -g <Resource Group> -n <AKS Cluster Name> --attach-acr <ACR Name>

# Check status of ACR integrated AKS 
az aks check-acr -g <resource group> -n <AKS Cluster Name> --acr <ACR Name>

# Detach existing ACR from an AKS Cluster
$ az aks update -g <resource group> -n <AKS Cluster Name> --detach-acr <ACR Name>
```


### Explore k8s context
```
# Use multiple kubeconfig files at the same time and view merged config
KUBECONFIG=~/.kube/config:~/.kube/kubconfig2

kubectl config view

# display list of contexts
kubectl config get-contexts                          

# display the current-context
kubectl config current-context                       

# set the default context to my-cluster-name
kubectl config use-context my-cluster-name           
```
