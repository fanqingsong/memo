# linux command

## commands

- [useful link](https://zhuanlan.zhihu.com/p/412735786)
- [cheat sheet](https://phoenixnap.com/kb/linux-commands-cheat-sheet)

### detect port service
```
nc -zv www.baidu.com 80
```

## view all service with ports
```
netstat -antulp
```

### create soft link
```
ln -sf /src /dst
```

### switch to root account if encountering such error
```
# PermissionError: [Errno 13] Permission denied

sudo su

sudo su - postgres
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

find . -type d -name __pycache__ -exec rm -r {} \;

find . | grep -E "(/__pycache__$|\.pyc$|\.pyo$)" | xargs rm -rf

find . -name "*.log" -mtime +5 -ok rm {} \;

find . -name "*.log" -exec mv {} .. \;

find . -name "*.log" -exec cp {} test3 \;

find /var/lib/docker/containers/ -name *-json.log
```

### rsync
```
rsync -avz /var/lib/docker /root/dockerlib/
```



