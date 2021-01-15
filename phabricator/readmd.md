

教程参考：

[https://www.jianshu.com/p/33383db134a2](https://www.jianshu.com/p/33383db134a2)


启动:

```
docker-compose up

docker-compose up -d


$ docker-compose down
$ docker-compose up
```

初始账号密码:

```
admin
Abc123456
```


## 问题1

>This request asked for "/" on host "localhost", but no site is configured which can serve this request.

```
docker exec -ti phabricator_phabricator_1 bash

/opt/bitnami/phabricator/bin/config set phabricator.base-uri 'http://172.16.23.82'

docker-compose restart
```

## 中文

```
docker exec -ti phabricator_phabricator_1 bash

cd /opt/bitnami/phabricator/src/extensions

创建 PhabricatorSimplifiedChineseTranslation.php 文件，内容：

https://raw.githubusercontent.com/phabricator-zh/phabricator/master/src/infrastructure/internationalization/translation/PhabricatorSimplifiedChineseTranslation.php

curl -O https://raw.githubusercontent.com/phabricator-zh/phabricator/master/src/infrastructure/internationalization/translation/PhabricatorSimplifiedChineseTranslation.php


docker-compose restart
```