
# docker 

## mirror

```
Docker mirror:
ubuntu@mlops:~/dify-1.0.1/docker$ cat /etc/docker/daemon.json
{
  "registry-mirrors": [
    "https://docker.zhai.cm",
    "https://a.ussh.net",
    "https://hub.littlediary.cn",
    "https://hub.rat.dev",
    "https://atomhub.openatom.cn",
    "https://docker.m.daocloud.io",
    "https://docker.1ms.run",
    "https://dytt.online",
    "https://func.ink",
    "https://lispy.org",
    "https://docker.xiaogenban1993.com",
    "https://docker.mybacc.com",
    "https://docker.yomansunter.com",
    "https://dockerhub.websoft9.com"
  ]
}
```

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

