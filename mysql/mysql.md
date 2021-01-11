
# 临时用

```
docker run --name global-mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=xxxx -d mysql:latest
```

连接： `0.0.0.0:3306`


# 添加 volume 持久化数据到本地

docker run --name tmp-mysql -v /Users/double/tmp/local/mysql:/var/lib/mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=xxxx -d mysql:latest


