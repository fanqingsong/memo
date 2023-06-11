
# docker image

## commands

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

### remove all unused image
```
docker image prune -a

docker system df

https://www.cnblogs.com/zjdxr-up/p/15769110.html
```




