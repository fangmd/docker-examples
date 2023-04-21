

## 注册用户

```
npm adduser --registry http://10.245.10.107:9200/
```


## Q

1. 注册用户的时候报 503 错误

```
npm config set noproxy localhost
npm config set noproxy [verdaccio 部署的ip地址]
```

2. 注册用户的时候卡住

```
可以通过查看 docker 日志，判断问题

docker logs -f xxxxx

可能是 htpasswd 文件权限有问题
```