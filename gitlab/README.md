

GitLab 本地启动，测试用

# 使用 docker-compose

```
docker-compose up -d
```

# 配置：

`.../gitlab/data/config/gitlab.rb`

```
external_url 'http://127.0.0.1'

gitlab_rails['time_zone'] = 'Asia/Shanghai'

### GitLab Shell settings for GitLab
gitlab_rails['gitlab_shell_ssh_port'] = 9022

puma['worker_processes'] = 2

# 本地测试用，优化内存占用
postgresql['shared_buffers'] = "512MB"
postgresql['max_connections'] = 200
prometheus_monitoring['enable'] = false

```

gitlab 更新配置&重启

```
gitlab-ctl reconfigure

gitlab-ctl restart
```

# 使用镜像启动

```
1. 拉取镜像
docker pull gitlab/gitlab-ce

2. 创建容器
docker run -d  -p 443:443 -p 80:80 -p 222:22 --name gitlab --restart always -v /home/gitlab/config:/etc/gitlab -v /home/gitlab/logs:/var/log/gitlab -v /home/gitlab/data:/var/opt/gitlab gitlab/gitlab-ce

docker run -d -p 9000:80 -p 222:22 --name gitlab --restart always -v /Users/double/soft/gitlab-data/config:/etc/gitlab -v /Users/double/soft/gitlab-data/logs:/var/log/gitlab -v /Users/double/soft/gitlab-data/data:/var/opt/gitlab gitlab/gitlab-ce

# -d：后台运行
# -p：将容器内部端口向外映射
# --name：命名容器名称
# -v：将容器内数据文件夹或者日志、配置等文件夹挂载到宿主机指定目录
```
