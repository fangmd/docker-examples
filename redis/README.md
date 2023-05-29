

## redis

```
docker run --name global-redis -d -p 6379:6379 -restart=always redis

docker run --name nodejs-redis -d -p 3021:6379 -restart=always redis
```

设置密码:

```
docker run --name nodejs-redis -d -p 3021:6379 -restart=always redis --requirepass fang2023
```


## redis cil

```
docker exec -it fec11ccf6078 bash

redis-cli
```