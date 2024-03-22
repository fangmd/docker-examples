
# 临时用

```
docker run --name global-mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=xxxx -d mysql:latest
```

连接： `0.0.0.0:3306`


# 添加 volume 持久化数据到本地

docker run --name tmp-mysql -v /Users/double/docker-column/mysql-data:/var/lib/mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=xxxx --restart=always -d mysql:latest

docker run --name tmp-mysql -v /Users/double/docker-column/mysql-data:/var/lib/mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=admin0224 --restart=always -d mysql:latest

docker run --name tmp-mysql -v /Users/double/docker-column/mysql-data:/var/lib/mysql -p 13306:3306 -e MYSQL_ROOT_PASSWORD=admin0224 --restart=always -d mysql:latest


docker run --name go-mysql -v /home/fang/docker-column/mysql-data:/var/lib/mysql -p 8111:3306 -e MYSQL_ROOT_PASSWORD=admin0224 --restart=always -d mysql:latest

