
# docker commands

## container

### view all containers
```
# for all running contianers
docker ps

# for all containers
docker ps -a
```

### remove one container
```
docker rm container_name
```

### remove all containers
```
docker rm $(docker ps -aq)
```

### stop one container
```
docker stop container_name
```

### stop all containers
```
docker stop $(docker ps -aq)
```

### stop all containers and remove them
```
docker stop $(docker ps -aq) & docker rm $(docker ps -aq)
```

### start one container
```
# for stopped container
docker start container_name

# for running container
docker restart container_name
```

### enter one running container
```
docker attach container_name
```

## image

### view all images
```
docker images
```

### remove one image
```
docker rmi image_name
```

### remove all images
```
docker rmi $(docker images -aq)
```

### build one image
```
docker build -t image_name .
```




