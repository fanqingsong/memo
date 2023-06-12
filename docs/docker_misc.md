
# docker 

## commands

### check disk of contianer
```
for i in $(docker ps -q ); do 
  echo "ContainerID: $i"; 
  ls -alh $(docker inspect $i | grep LogPath|awk -F "\"" '{print $4}');
done;
```

### find the most sized container
```
cd /var/lib/docker/containers
du -a --max-depth=1 | sort -nr | head -5
```

### check and clean disk of contianer
```
docker inspect --format='{{.LogPath}}' my-app
 sudo sh -c 'echo "" > $(docker inspect --format="{{.LogPath}}" my-app)'
```

