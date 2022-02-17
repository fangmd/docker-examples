



```
docker pull jenkins/jenkins

docker container run --name jenkins -p 9080:8080 -p 50000:50000 -v /Users/double/jenkins:/var/jenkins_home -d jenkins/jenkins


docker container run --name jenkins2 -p 9080:8080 -p 50000:50000 -v /Users/double/jenkins:/var/jenkins_home -d jenkins/jenkins:2.333
```

