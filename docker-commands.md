## Basic Docker Commands

### Docker Build
```
docker build -t mycoolimage:1.0 .
```

### Docker Build Specifiy Dockerfile
```
docker build -f /home/me/myapp/dockerfiles/debug /home/me/myapp
docker build -f ../../../../dockerfiles/debug /home/me/myapp
```

### Docker Run
```
docker run –d –p 8090:8082  --name contaniner1 imagedemo:1.0
```

### Run Commands Inside Container
```
docker exec –it <Container Id> /bin/bash
docker exec –it <Container Id> cmd
docker run –it <Image Id> cmd
```
