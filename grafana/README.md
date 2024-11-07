

# install

```shell
# create a directory for your data
mkdir data

# start grafana with your user id and using the data directory
docker run -d -p 3005:3000 --name=grafana \
  --user "$(id -u)" \
  --volume "$PWD/data:/var/lib/grafana" \
  grafana/grafana-enterprise
  
```