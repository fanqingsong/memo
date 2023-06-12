# linux command

## commands

- [useful link](https://zhuanlan.zhihu.com/p/412735786)


### detect port service
```
nc -zv www.baidu.com 80
```

### create soft link
```
ln -sf /src /dst
```

### switch to root account if encountering such error
```
# PermissionError: [Errno 13] Permission denied

sudo su
```

### check disk size
```
df -h
```

### find the subdirectory size of root
```
du -hx --max-depth=1 / | sort -h -r

https://www.cnblogs.com/z1990/p/15179901.html
```

### find older files and ....
```
https://www.cnblogs.com/peida/archive/2012/11/14/2769248.html

find . -type f -exec ls -l {} \;

find . -type f -mtime +14 -exec rm {} \; 

find . -name "*.log" -mtime +5 -ok rm {} \;

find . -name "*.log" -exec mv {} .. \;

find . -name "*.log" -exec cp {} test3 \;

find /var/lib/docker/containers/ -name *-json.log
```

### rsync
```
rsync -avz /var/lib/docker /root/dockerlib/
```



