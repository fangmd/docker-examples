



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

查看 docker 所有网络:

```
docker network ls
```

创建自定义网络:

```
docker network create --subnet=172.20.0.0/16 centos-network
```

# 容器

1. 进入容器

```
docker exec -it [container_name] /bin/bash
```
