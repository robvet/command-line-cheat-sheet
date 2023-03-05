## Basic Docker Commands

### Docker Build
```
docker build -t mycoolimage:1.0 .
```

### Docker Build - Dockerfile in Different Subfolder
```
docker build -t mycoolimage:1.0 -f subfolder/Dockerfile .
docker build -f ../../subfolder/Dockerfile .
```

### Docker Run
```
// Port mapping: (8090:80 maps to HostPort:ContainerPort)
docker run –d –p 8090:80  --name contaniner1 imagedemo:1.0

// add local Docker network with 'net' command
docker run -d -p 3000:3000 --name web --net fabmedical content-web
```

### Push Docker Image to Registry
```
// First, tag image
docker tag <name of image> <name of ACR>/<namespace>/<name of image>

// Example of tagging image
docker tag content-web peteacr01.azurecr.io/wthaks/content-web

// Push image to registry
docker push <name of ACR>/<namespace>/<name of image> 

// Example of pushing image
docker push peteacr01.azurecr.io/wthaks/content-web 

// List images in repository
az acr repository list --name <name of ACR>
```

### Destructive Comands
```
// Kill a container
docker kill <container id>

// Kill dangling imafges
docker image prune 

// add local Docker network with 'net' command
docker run -d -p 3000:3000 --name web --net fabmedical content-web
```

### Run Commands Inside Container
```
docker exec –it <Container Id> /bin/bash
docker exec –it <Container Id> cmd
docker run –it <Image Id> cmd
```
