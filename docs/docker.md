
# commands

## container

### view all container
```
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


