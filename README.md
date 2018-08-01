## Docker for development

### Folder structure
```
- .docker
    Dockerfile
    - html
        index.html
```
### Build coder image
```
docker build -t docker-session-nginx .docker/
```

### Run docker container
```
docker run --name nginx-demo -d -p 8080:80 docker-session-nginx
```

### View docker process
```
docker ps
```
