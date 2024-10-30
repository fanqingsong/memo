
# docker container

## commands

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

### remove all containers
```
docker container prune
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
# for iterative runing container
docker attach container_name

# for all container
docker exec -it container_name /bin/bash
```

### export and import container
```
# export
# https://www.cnblogs.com/yanling-coder/p/11715534.html
docker export b91d9ad83efa > tomcat80824.tar

# import
docker import tomcat80824.tar
docker tag 880f tomcat80824:1.0
```



