---
sidebar_position: 10
---

# Filebeat

[官方文档](https://www.elastic.co/guide/en/beats/filebeat/7.3/filebeat-configuration.html)

# 安装

```
docker pull docker.elastic.co/beats/filebeat:8.0.0

运行容器:

```
docker run -d \
--name=filebeat \
-v /Users/double/projects/docker-examples/filebeat/filebeat.yml:/usr/share/filebeat/filebeat.yml \
-v /Users/double/projects/express-template/logs:/var/log/filebeat/ \
docker.elastic.co/beats/filebeat:8.0.0 filebeat


docker run -d \
--name=filebeat-nginx \
-v /root/filebeat-nginx/filebeat.yml:/usr/share/filebeat/filebeat.yml \
-v /var/log/nginx:/var/log/filebeat/ \
docker.elastic.co/beats/filebeat:8.0.0 filebeat
```


