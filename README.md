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
### Helpful commands
```
//view all docker images stored on your local 

docker images -a

//delete a specific image 
docker rmi <image-id>

//delete a specific container 
docker rm <container id>

//ssh inside the docker
docker exec -i -t <container name> bash

//start a existing docker container
docker start <container name>

//stop a running container
docker stop <container name>

//create htpasswd
perl -le 'print crypt("password", "METHOD_SHA512")'
```
### Push a docker image to docker hub repository
```
docker login --username=<username> --email=<your emailid>
docker tag <image-id> <docker-hub-username>/<local-image-name>:<tag-name>
docker push <docker-hub-username>/<local-image-name>
```

### Run docker compose
```
//run docker compose 
docker-compose up

//run docker compose as daemon
docker-compose up -d

//view container running
docker-compose ps
```