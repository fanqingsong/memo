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

# check appname and pid
sudo netstat -antulp

sudo ss -tulnp | grep 443
```

## view process info
```
ps aux | grep pid
```

## scp command
```
#下载设备中 root 目录下的 test.txt 到当前目录
scp root@192.168.0.111:/root/test.txt ./

 #从设备下载 root 目录下的 demo 文件夹到当前目录
scp -r root@192.168.0.111:/root/demo ./

#上传当前目录下的 result.log 到设备 root 目录下
scp ./result.log root@192.168.0.111:/root/ 

#上传当前目录下的 check 目录到设备 root 目录
scp -r ./check root@192.168.0.111:/root/
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

sudo -i -u senthil
```

### user group
```
sudo adduser senthil

sudo usermod -g root song

sudo adduser senthil sudo
sudo usermod -aG sudo senthil

sudo deluser senthil
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

find ./ -size +10M -size -20M

find ~ -size -1G
```

### rsync
```
rsync -avz /var/lib/docker /root/dockerlib/
```

### grep
```
grep nobody /etc/passwd

grep linuxtechi /etc/passwd /etc/shadow /etc/gshadow

# list all files
grep -l 'root' /etc/fstab /etc/passwd /etc/mtab

# display line number
grep -n 'nobody' /etc/passwd

# find string with prefix
grep ^backup /etc/passwd

# find string with suffix
grep bash$ /etc/passwd

# find recursively
sudo grep -r nobody /etc

# find empty line
grep '^$' /etc/sysctl.conf

# ignore lettercase
grep -i IP_Forward /etc/sysctl.conf

# find with one word
sudo sysctl -a | grep -w 'vm.swappiness'

# find with multiple words
grep -e nobody -e mail /etc/passwd
grep -E "nobody|mail" /etc/passwd

```




