



# 镜像

## Dockerfile 构建镜像

按照当前目录下的 `Dockerfile` 构建镜像

```
docker build -t centos:8 .
```

1. `-t` 设置镜像名称

## 使用镜像创建容器

```
docker run -t -i centos:8
```

1. `-t`

创建容器并设置置顶 ip:

```
docker run -itd --name double-centos --net centos-network --ip 172.20.0.2 centos:8
```

1. `--name` 设置容器名称
2. `centos:8` 镜像名称

查看容器ip：

```
docker inspect double-centos
```

重启容器:

```
docker restart gitlab
```


# 网络

1. 查看 docker 所有网络:

```
docker network ls
```

2. 创建自定义网络:

```
docker network create --subnet=172.20.0.0/16 centos-network
```

3. 访问宿主机网络

```
使用 host.docker.internal 代替 127.0.0.1
```


# 容器

1. 进入容器

```
docker exec -it [container_name] /bin/bash
```

2. 进入容器，使用 root 用户

```
docker exec -u 0 -it [container_name] bash
docker exec -u 0 -it 4199bbe484ba bash
```

# 日志

时时查看日志：

```
docker logs --tail 1000 -f [container_name]
```