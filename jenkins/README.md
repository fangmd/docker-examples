



```
docker pull jenkins/jenkins

docker container run --name jenkins -p 9080:8080 -p 50000:50000 -v /Users/double/jenkins:/var/jenkins_home -d jenkins/jenkins
```

